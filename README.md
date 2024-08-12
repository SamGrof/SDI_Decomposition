Index Decomposition of the Drivers Behind the Sustainable Development Index of Costa Rica (1990-2022)

Costa Rica has the highest Sustainable Development Index (SDI) of all countries (Hickel, Jason. 2020). In this work, we aim to gain insights into the material conditions and sociometabolic patterns behind this success. 

The carried out analysis, the summary of the results, along with a broader discussion and outlook, can be found in the Jupyter notebook script "SDI_Index_Decomposition_Costa_Rica_July_24.ipynb." In the following, we outline the current state of the literature and introduce our methods.

Note: This is not a peer-reviewed scientific work. It aims to demonstrate the author’s (Simon Graf) ability to work scientifically with Python, data, and GitHub. However, the ideas developed and the analysis carried out are original and offer a promising approach to understanding the metabolic patterns of Costa Rica and sustainable development pathways in general.

--- Introduction ---

The SDI is designed as an ecological extension of the Human Development Index, representing a condensed, one-dimensional version of the Safe and Just Space concept (O'Neil et al., 2018). The SDI is a quotient, SDI = DI / EII, where DI is the Development Index (a condensed measure of Education, Life Expectancy, and Income) and EII is the Ecological Impact Index (measuring the transgression of the GHG Planetary Boundary and the Material Footprint Planetary Boundary). For more details, visit https://www.sustainabledevelopmentindex.org/methods. By juxtaposing social and ecological achievements and pressures against the corresponding social and ecological (planetary) boundaries, these concepts aim to measure socio-ecological success and the (strong) sustainability of individual countries. It is worth noting that no country has yet achieved a sufficient degree of success. However, Costa Rica, among a few other countries, is on a promising (acceptable) pathway. The socio-metabolic patterns behind these promising pathways remain largely unexplored.

Both concepts are rooted in a Provisioning Systems (PS) perspective, where the economy is understood as a hierarchical process from resource extraction (ends) to societal well-being (means). The concept of PS is closely tied to the field of Ecological Economics and can be traced back to Daly's 'End-Mean Spectrum' (Daly, 1977). The theoretical idea is to examine not only the ultimate ends and means but also the intermediate stages in the economic process. This includes tracing energy and material flows through process stages, measuring throughput, intensities, and efficiencies. There are theoretical works covering this (Plank et al., 2021) and some implementations of a full process stage view (Tanikawa et al., 2021). However, empirical works that possess both (1) a multi-dimensional view on ecological boundaries and social achievements, and (2) a consistent inclusion of process stages, are still rare.

The hierarchical concept of PS makes it suitable for a certain type of analysis: Index Decomposition Analysis (Tanikawa et al., 2021).

--- Methods ---

In the following, we introduce environmental-economic Material Flow Analysis (ewMFA) indicators into the SDI equation to perform an analysis of Costa Rica's sociometabolic patterns.

We are particularly interested in the Material Footprint (MF) and Domestic Material Consumption (DMC), which are necessary to sustain Costa Rica's society and its high SDI. We choose both MF and DMC to gain a better understanding of Costa Rica's role in the global economy. Additionally, we aim to investigate possible drivers of the SDI:

    Social Material Intensity (DI/DMC): This measures how material-intensive the well-being of Costa Rica is.
    Economic Internalization Rate (DMC/MF): This compares the production-based throughput to the consumption-based throughput of materials.
    Ecological Material Efficiency (MF/EII): This measures the ecological impact per tonne of material used.

Inserting these drivers into the SDI equation yields:

SDI=DI/EII=(DI/DMC)×(DMC/MF)×(MF/EII)

We now relate the SDI to its drivers. The mathematical trick applied here is to insert a "1" into a multiplication. When multiplying out, the MF and DMC terms cancel each other out, ensuring consistency. The equation now takes a similar form to the "Kaya Identity," making the drivers analyzable.

Note: Using MF and DMC is just a first step to gain an overall aggregated perspective and acts as proof of concept. It is possible to insert multiple process stages, as well as stocks in addition to flows (Tanikawa et al., 2021). Further exploration of disaggregated flows (linked to sectors) and the inclusion of an energy (exergy) perspective is possible and intended for future work. This framework also allows for cross-country analysis to identify SDI drivers on a global scale.

--- Analysis and Results ---

We analyze the SDI and its sociometabolic patterns over the period from 1990 to 2022. A summary of the results, along with broader discussion and outlook, can be found in the Jupyter notebook script "SDI_Index_Decomposition_Costa_Rica_July_24.ipynb".
Literature

- Daly, Hermann E. 1977. "Steady-state economics: the economics of biophysical equilibrium and moral growth"
- Hickel, Jason. 2020. “The Sustainable Development Index: Measuring the Ecological Efficiency of Human Development in the Anthropocene,”
- Tanikawa, Hiroki et al. 2021. A framework of indicators for associating material stocks and flows to service provisioning: Application for     Japan 1990–2015
- Plank, Babara et al. 2021. "Doing more with less: Provisioning systems and the transformation of the stock-flow-service nexus"
