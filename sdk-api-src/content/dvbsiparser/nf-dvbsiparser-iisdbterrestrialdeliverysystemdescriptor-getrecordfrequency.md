---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency
title: IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency (dvbsiparser.h)
author: windows-sdk-content
description: Gets the center frequency from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_getrecordfrequency.htm
tech.root: mstv
ms.assetid: 9040dcc9-49c8-4c3b-ad86-7dc38d1722b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordFrequency, GetRecordFrequency method [Microsoft TV Technologies], GetRecordFrequency method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetRecordFrequency method, IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency, IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency, mstv.iisdbterrestrialdeliverysystemdescriptor_getrecordfrequency
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency


## -description


Gets the center frequency from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/72dcfb91-4137-4149-b30d-2551cb209688">IIsdbTerrestrialDeliverySystemDescriptor::GetCountOfRecords</a>



### -param pdwVal [out]

Receives the center frequency, in units of 1/7 MHz. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32bde3dd-05e0-466b-9f04-4b55b0d7f374">IIsdbTerrestrialDeliverySystemDescriptor</a>
 

 

