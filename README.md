Rock-Paper-Scissors-Lizard-Spock


{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "ProjectRPSLSPO.ipynb",
      "provenance": [],
      "collapsed_sections": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "qVL9v80Tw174"
      },
      "source": [
        "# **Rock - Paper - Scissors - Lizard - Spock**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "-85cz4_mvwKh"
      },
      "source": [
        "import random                                                                          # importing the library"
      ],
      "execution_count": 4,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "LLdXfP6dyvJN"
      },
      "source": [
        "![Rock_paper_scissors_lizard_spock.png](data:image/png;base64,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)"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "E6dpUaqBzBq_"
      },
      "source": [
        "**r = Rock, p = Paper, s = Scissors, l = Lizard, spo = Spock**"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "JEftzKbZxEj_",
        "outputId": "927b0585-1310-443c-8b78-14a4ff8b7c7f"
      },
      "source": [
        "begin = 'y'                                                                           \n",
        "while begin.lower() == 'y':\n",
        "   moves = ['r','p','s', 'l', 'spo']                                                                           # possible moves\n",
        "   player_wins = ['pr','sp','rs', 'lp', 'lspo', 'spos','spor', 'rl', 'sl','pspo']                              # winning possibility\n",
        "   player_moves = input('Enter your move \"r = Rock, p = Paper, s = Scissors, l = Lizard, spo = Spock:\"')      # user input\n",
        "   computer_moves = random.choice(moves)                                                                       # random computer moves from random.choices\n",
        "   print(\"Computer's move is {} :\".format('computer_moves'))                                                   # printing through string formatting method\n",
        "   print(\"Player's move is: %s\" %(player_moves))                                                               # printing through string formatting method       \n",
        "    \n",
        "   if player_moves == computer_moves:                                                                          # Implementing NestedIf loop  \n",
        "       print(\"tie\")\n",
        "   elif player_moves + computer_moves in player_wins:\n",
        "       print(\"you win\")\n",
        "   else: \n",
        "       print(\"you lose\")\n",
        "  \n",
        "   begin = input(\"Do you want to continue? y = yes, q = quit : \")                      # taking user input in the variable begin that whether to continue the game or not\n",
        "   if begin.lower() == 'q':                                                            # converting the input to lower case and implenting if and break. \n",
        "       break"
      ],
      "execution_count": 8,
      "outputs": [
        {
          "name": "stdout",
          "output_type": "stream",
          "text": [
            " Enter your move \"r = Rock, p = Paper, s = Scissors, l = Lizard, spo = Spock:\"r\n",
            "Computer's move is computer_moves :\n",
            "Player's move is: r\n",
            "you win\n",
            "Do you want to continue? y = yes, q = quit : y\n",
            " Enter your move \"r = Rock, p = Paper, s = Scissors, l = Lizard, spo = Spock:\"spo\n",
            "Computer's move is computer_moves :\n",
            "Player's move is: spo\n",
            "you lose\n",
            "Do you want to continue? y = yes, q = quit : q\n"
          ]
        }
      ]
    }
  ]
} 
