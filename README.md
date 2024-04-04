# PcsBatteryOptimaization
自家消費蓄電池容量の最適化方法（電力予測や需要予測を使わず、太陽光発電電力と消費電力（分毎のデータ） Battery Optimaization(for Critical Load &amp; Not Reverse Currrent to Grid)  
この文書は、自家消費用蓄電池の容量を最適化するための方法に関するものです。電力予測や需要予測を使用せず、太陽光発電と消費電力のデータ（分毎）を利用しています。文書では、MATLABを使用してデータの分析やグラフの作成方法が説明されており、PandasとMatplotlibを用いたデータ処理と可視化の例が示されています。

主に、1分間隔で収集された太陽光発電量と消費電力量のデータを分析し、これらのデータから電力の差（発電電力から消費電力を引いた値）を計算しています。この差は、蓄電池の充放電に関わる主要な指標です。文書では、この差を用いて、日々や月々の電力使用パターンを評価し、蓄電池の充放電サイクルを最適化する方法を示しています。

また、負の値（消費電力が発電電力を上回る場合）を特に分析し、これらの値の分布を調べることで、必要な蓄電池容量の見積もりに役立てています。これにより、夜間の電力需要を満たすために必要な最小限の蓄電池容量を推定し、雨天時の連続した日々に対する蓄電池の容量要求を評価しています。

最後に、負の累積和の大きさを分析することで、蓄電池の容量がどれほどあれば十分かを評価しており、さらに、累積和が特定の閾値を超えるか、または下回る場合のシナリオをシミュレーションしています。これにより、蓄電池の最適容量設定に関する洞察を提供し、太陽光発電を利用した自家消費システムの効率化を目指しています。

Here is an English translation:

This document describes a method for optimizing the capacity of a battery for self-consumption, without using power or demand forecasting. It utilizes data on solar power generation and power consumption (at one-minute intervals). The document explains how to analyze the data and create graphs using MATLAB, and provides examples of data processing and visualization using Pandas and Matplotlib.

Primarily, it analyzes the solar power generation and power consumption data collected at one-minute intervals. It calculates the difference between these two (generation minus consumption), which is a crucial indicator for battery charging and discharging. The document demonstrates how to evaluate the daily and monthly power usage patterns using this difference and optimize the battery charge and discharge cycles.

Additionally, it particularly analyzes negative values (when consumption exceeds generation) and examines their distribution to estimate the required battery capacity. This helps determine the minimum battery capacity needed to meet nighttime power demands and assess the capacity requirements for consecutive rainy days.

Furthermore, by analyzing the magnitude of the negative cumulative sum, it evaluates whether a given battery capacity would be sufficient. It also simulates scenarios where the cumulative sum exceeds or falls below a certain threshold. This provides insights into optimal battery capacity settings, aiming to improve the efficiency of self-consumption systems utilizing solar power generation.