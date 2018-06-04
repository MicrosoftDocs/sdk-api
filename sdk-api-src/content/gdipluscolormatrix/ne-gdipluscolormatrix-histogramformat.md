---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# HistogramFormat enumeration


## -description


The <b>HistogramFormat</b> enumeration specifies the number and type of histograms that represent the color channels of a bitmap. This enumeration is used with the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method.


## -enum-fields




### -field HistogramFormatARGB

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns four histograms: one each for the alpha, red, green, and blue channels. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The red-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The green-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The blue-channel histogram is written to the buffer pointed to by the <i>channel3</i> parameter.


### -field HistogramFormatPARGB

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns four histograms: one each for the alpha, red, green, and blue channels. The red, green, and blue channels are each multiplied by the alpha channel before the histograms are created. The bitmap is not permanently altered when the color channels are multiplied by the alpha channel; that multiplication is only for the purpose of creating the histograms. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The red-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The green-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The blue-channel histogram is written to the buffer pointed to by the <i>channel3</i> parameter.


### -field HistogramFormatRGB

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns three histograms: one each for the red, green, and blue channels. The red-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The green-channel histogram is written to the buffer pointed to by the <i>channel1</i> parameter. The blue-channel histogram is written to the buffer pointed to by the <i>channel2</i> parameter.  The <i>channel3</i> parameter must be set to <b>NULL</b>.


### -field HistogramFormatGray

Specifies that each pixel is converted to a grayscale value in the range 0 through 255, and then one histogram, based on those grayscale value, is returned. The bitmap is not permanently altered by the conversion to grayscale values; those values are calculated only for the purpose of creating the histogram. The grayscale histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.


### -field HistogramFormatB

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns a histogram for the blue channel. The blue-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.


### -field HistogramFormatG

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns a histogram for the green channel. The green-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.


### -field HistogramFormatR

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns a histogram for the red channel. The red-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.


### -field HistogramFormatA

Specifies that the <a href="https://msdn.microsoft.com/c7dcc384-54b1-457a-86cd-e27b232a9152">Bitmap::GetHistogram</a> method returns a histogram for the alpha channel. The alpha-channel histogram is written to the buffer pointed to by the <i>channel0</i> parameter of the <b>Bitmap::GetHistogram</b> method. The <i>channel1</i>, <i>channel2</i>, and <i>channel3</i> parameters must be set to <b>NULL</b>.

