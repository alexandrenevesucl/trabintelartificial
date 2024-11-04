******************************************************************************************

# HTRU2

Author: Rob Lyon, School of Computer Science & Jodrell Bank Centre for Astrophysics,
		University of Manchester, Kilburn Building, Oxford Road, Manchester M13 9PL.

Contact:	rob@scienceguyrob.com or robert.lyon@.manchester.ac.uk
Web:		http://www.scienceguyrob.com or http://www.cs.manchester.ac.uk
			or alternatively http://www.jb.man.ac.uk
******************************************************************************************

1. Overview

	HTRU2 is a data set which describes a sample of pulsar candidates collected during the
	High Time Resolution Universe Survey (South) [1]. 
	
	Pulsars are a rare type of Neutron star that produce radio emission detectable here on
	Earth. They are of considerable scientific interest as probes of space-time, the inter-
	stellar medium, and states of matter (see [2] for more uses). 
	
	As pulsars rotate, their emission beam sweeps across the sky, and when this crosses
	our line of sight, produces a detectable pattern of broadband radio emission. As pulsars
	rotate rapidly, this pattern repeats periodically. Thus pulsar search involves looking
	for periodic radio signals with large radio telescopes.
	
	Each pulsar produces a slightly different emission pattern, which varies slightly with each
	rotation (see [2] for an introduction to pulsar astrophysics to find out why). Thus a 
	potential signal detection known as a 'candidate', is averaged over many rotations of the
	pulsar, as determined by the length of an observation. In the absence of additional info,
	each candidate could potentially describe a real pulsar. However in practice almost all
	detections are caused by radio frequency interference (RFI) and noise, making legitimate
	signals hard to find.
	
	Machine learning tools are now being used to automatically label pulsar candidates to
	facilitate rapid analysis. Classification systems in particular are being widely adopted,
	(see [4,5,6,7,8,9]) which treat the candidate data sets  as binary classification problems.
	Here the legitimate pulsar examples are a minority positive class, and spurious examples
	the majority negative class. At present multi-class labels are unavailable, given the
	costs associated with data annotation.
	
	The data set shared here contains 16,259 spurious examples caused by RFI/noise, and 1,639
	real pulsar examples. These examples have all been checked by human annotators. Each
	candidate is described by 8 continuous variables. The first four are simple statistics
	obtained from the integrated pulse profile (folded profile). This is an array of continuous
	variables that describe a longitude-resolved version of the signal that has been averaged
	in both time and frequency (see [3] for more details). The remaining four variables are
	similarly obtained from the DM-SNR curve (again see [3] for more details). These are 
	summarised below:
	
	1. Mean of the integrated profile.
	2. Standard deviation of the integrated profile.
	3. Excess kurtosis of the integrated profile.
	4. Skewness of the integrated profile.
	5. Mean of the DM-SNR curve.
	6. Standard deviation of the DM-SNR curve.
	7. Excess kurtosis of the DM-SNR curve.
	8. Skewness of the DM-SNR curve.
	
	HTRU 2 Summary
	
	17,898 total examples.
	1,639 positive examples.
	16,259 negative examples.
	
	
	The data is presented in two formats: CSV and ARFF (used by the WEKA data mining tool).
	Candidates are stored in both files in separate rows. Each row lists the variables first,
	and the class label is the final entry. The class labels used are 0 (negative) and 1 
	(positive).
	
	Please not that the data contains no positional information or other astronomical details. It is 
	simply feature data extracted from candidate files using the PulsarFeatureLab tool (see [10]).

2. Citing our work	
	
	If you use the dataset in your work please cite us using the DOI of the dataset, and the paper:
	
	R. J. Lyon, B. W. Stappers, S. Cooper, J. M. Brooke, J. D. Knowles, Fifty Years of Pulsar
	Candidate Selection: From simple filters to a new principled real-time classification approach
	MNRAS, 2016.
	
3. Acknowledgements

	This data was obtained with the support of grant EP/I028099/1 for the University of Manchester 
	Centre for Doctoral Training in Computer Science, from the UK Engineering and Physical Sciences
	Research Council (EPSRC). The raw observational data was collected by the High Time Resolution
	Universe Collaboration using the Parkes Observatory, funded by the Commonwealth of Australia and
	managed by the CSIRO.
	
4. References

	[1] M.~J. Keith et al., "The High Time Resolution Universe Pulsar Survey - I. System Configuration 
	    and Initial Discoveries",2010, Monthly Notices of the Royal Astronomical Society, vol. 409,
	    pp. 619-627. DOI: 10.1111/j.1365-2966.2010.17325.x
	
	[2] D. R. Lorimer and M. Kramer, "Handbook of Pulsar Astronomy", Cambridge University Press, 2005.
	
	[3] R. J. Lyon, "Why Are Pulsars Hard To Find?", PhD Thesis, University of Manchester, 2015.
	
	[4] R. J. Lyon et al., "Fifty Years of Pulsar Candidate Selection: From simple filters to a new
		principled real-time classification approach", Monthly Notices of the Royal Astronomical Society,
		submitted.
		
	[5] R. P. Eatough et al., "Selection of radio pulsar candidates using artificial neural networks",
		Monthly Notices of the Royal Astronomical Society, vol. 407, no. 4, pp. 2443-2450, 2010.
		
	[6] S. D. Bates et al., "The high time resolution universe pulsar survey vi. an artificial neural
		network and timing of 75 pulsars", Monthly Notices of the Royal Astronomical Society, vol. 427,
		no. 2, pp. 1052-1065, 2012.

	[7] D. Thornton, "The High Time Resolution Radio Sky", PhD thesis, University of Manchester,
		Jodrell Bank Centre for Astrophysics School of Physics and Astronomy, 2013.
		
	[8] K. J. Lee et al., "PEACE: pulsar evaluation algorithm for candidate extraction a software package
		for post-analysis processing of pulsar survey candidates", Monthly Notices of the Royal Astronomical
		Society, vol. 433, no. 1, pp. 688-694, 2013.
		
	[9] V. Morello et al., "SPINN: a straightforward machine learning solution to the pulsar candidate
		selection problem", Monthly Notices of the Royal Astronomical Society, vol. 443, no. 2,
		pp. 1651-1662, 2014.
		
	[10] R. J. Lyon, "PulsarFeatureLab", 2015, https://dx.doi.org/10.6084/m9.figshare.1536472.v1.



TRADUÇÃO 

1. Visão geral

	HTRU2 é um conjunto de dados que descreve uma amostra de candidatos a pulsares coletados durante o
	Pesquisa do Universo de Alta Resolução de Tempo (Sul) [1]. 
	
	Os pulsares são um tipo raro de estrela de nêutrons que produz emissões de rádio detectáveis ​​aqui no
	Terra. Eles são de considerável interesse científico como sondas do espaço-tempo, da inter-
	meio estelar e estados da matéria (veja [2] para mais usos). 
	
	À medida que os pulsares giram, o seu feixe de emissão percorre o céu e, quando este atravessa
	nossa linha de visão, produz um padrão detectável de emissão de rádio em banda larga. Como pulsares
	gire rapidamente, esse padrão se repete periodicamente. Assim, a busca do pulsar envolve olhar
	para sinais de rádio periódicos com grandes radiotelescópios.
Cada pulsar produz um padrão de emissão ligeiramente diferente, que varia ligeiramente com cada
	rotação (veja [2] para uma introdução à astrofísica de pulsares para descobrir o porquê). Assim um 
	detecção de sinal potencial, conhecida como 'candidato', é calculada a média de muitas rotações do
	pulsar, conforme determinado pela duração de uma observação. Na ausência de informações adicionais,
	cada candidato poderia potencialmente descrever um pulsar real. Contudo, na prática, quase todos
	as detecções são causadas por interferência de radiofrequência (RFI) e ruído, tornando legítimo
	sinais difíceis de encontrar.
	
	Ferramentas de aprendizado de máquina agora estão sendo usadas para rotular automaticamente candidatos a pulsares para
	facilitar análises rápidas. Os sistemas de classificação, em particular, estão a ser amplamente adoptados,
	(ver [4,5,6,7,8,9]) que tratam os conjuntos de dados candidatos como problemas de classificação binária.
	Aqui, os exemplos legítimos de pulsares são uma classe positiva minoritária, e exemplos espúrios
	a classe majoritária negativa. Actualmente, os rótulos multiclasse não estão disponíveis, dada a
	custos associados à anotação de dados.

O conjunto de dados compartilhado aqui contém 16.259 exemplos espúrios causados ​​por RFI/ruído e 1.639
	exemplos reais de pulsares. Todos esses exemplos foram verificados por anotadores humanos. Cada
	candidato é descrito por 8 variáveis ​​contínuas. Os quatro primeiros são estatísticas simples
	obtido a partir do perfil de pulso integrado (perfil dobrado). Esta é uma matriz de contínuo
	variáveis ​​que descrevem uma versão resolvida em longitude do sinal cuja média foi calculada
	tanto no tempo quanto na frequência (veja [3] para mais detalhes). As quatro variáveis ​​restantes são
	obtido de forma semelhante a partir da curva DM-SNR (ver novamente [3] para mais detalhes). Estes são 
	resumido abaixo:


1. Média do perfil integrado.
	2. Desvio padrão do perfil integrado.
	3. Excesso de curtose do perfil integrado.
	4. Distorção do perfil integrado.
	5. Média da curva DM-SNR.
	6. Desvio padrão da curva DM-SNR.
	7. Excesso de curtose da curva DM-SNR.
	8. Assimetria da curva DM-SNR.
	
	Resumo do HTRU2
	
	17.898 exemplares no total.
	1.639 exemplos positivos.
	16.259 exemplos negativos.

Os dados são apresentados em dois formatos: CSV e ARFF (utilizado pela ferramenta de mineração de dados WEKA).
	Os candidatos são armazenados em ambos os arquivos em linhas separadas. Cada linha lista as variáveis ​​primeiro,
	e o rótulo da classe é a entrada final. Os rótulos de classe usados ​​são 0 (negativo) e 1 
	(positivo).
	
	Observe que os dados não contêm informações de posição ou outros detalhes astronômicos. Isso é 
	simplesmente apresente dados extraídos de arquivos candidatos usando a ferramenta PulsarFeatureLab (ver [10]).

2. Citando nosso trabalho	
	
	Se você usar o conjunto de dados em seu trabalho, cite-nos usando o DOI do conjunto de dados e o artigo:
	
	RJ Lyon, BW Stappers, S. Cooper, JM Brooke, JD Knowles, Cinquenta Anos de Pulsar
	Seleção de Candidatos: De filtros simples a uma nova abordagem de classificação em tempo real baseada em princípios
	MNRAS, 2016.
	
3. Agradecimentos

	Estes dados foram obtidos com o apoio da bolsa EP/I028099/1 para a Universidade de Manchester 
	Centro de Treinamento Doutoral em Ciência da Computação, da Engenharia e Ciências Físicas do Reino Unido
	Conselho de Pesquisa (EPSRC). Os dados observacionais brutos foram coletados pelo High Time Resolution
	Colaboração Universe usando o Observatório Parkes, financiado pela Commonwealth da Austrália e
	gerenciado pelo CSIRO.
