---
UID: NF:bdaiface.IFrequencyMap.put_FrequencyMapping
title: IFrequencyMap::put_FrequencyMapping (bdaiface.h)
description: The put_FrequencyMapping method sets the frequency table.
helpviewer_keywords: ["IFrequencyMap interface [Microsoft TV Technologies]","put_FrequencyMapping method","IFrequencyMap.put_FrequencyMapping","IFrequencyMap::put_FrequencyMapping","IFrequencyMapput_FrequencyMapping","bdaiface/IFrequencyMap::put_FrequencyMapping","mstv.ifrequencymap_put_frequencymapping","put_FrequencyMapping","put_FrequencyMapping method [Microsoft TV Technologies]","put_FrequencyMapping method [Microsoft TV Technologies]","IFrequencyMap interface"]
old-location: mstv\ifrequencymap_put_frequencymapping.htm
tech.root: mstv
ms.assetid: cfde2c8e-803d-46b8-b3d4-8e9b3129af0e
ms.date: 12/05/2018
ms.keywords: IFrequencyMap interface [Microsoft TV Technologies],put_FrequencyMapping method, IFrequencyMap.put_FrequencyMapping, IFrequencyMap::put_FrequencyMapping, IFrequencyMapput_FrequencyMapping, bdaiface/IFrequencyMap::put_FrequencyMapping, mstv.ifrequencymap_put_frequencymapping, put_FrequencyMapping, put_FrequencyMapping method [Microsoft TV Technologies], put_FrequencyMapping method [Microsoft TV Technologies],IFrequencyMap interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFrequencyMap::put_FrequencyMapping
 - bdaiface/IFrequencyMap::put_FrequencyMapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IFrequencyMap.put_FrequencyMapping
---

# IFrequencyMap::put_FrequencyMapping


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FrequencyMapping</b> method sets the frequency table.

## -parameters

### -param ulCount [in]

Specifies the size of the array given in <i>pList</i>.

### -param pList [in]

Address of an array of size <i>ulCount</i>, allocated by the caller. The array should contain a list of all the frequencies (in kHz) that are valid in the current country/region.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Applications can use this method to modify a frequency table or create new frequency tables. The changes are not stored by the Network Provider; the application must store the information itself and call <b>put_FrequencyMapping</b> each time the Network Provider is created.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ifrequencymap">IFrequencyMap Interface</a>