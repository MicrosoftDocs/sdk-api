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

# OleConvertIStorageToOLESTREAM function


## -description



			The 
<b>OleConvertIStorageToOLESTREAM</b> function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model but does not include the presentation data. This is one of several compatibility functions.


## -parameters




### -param pstg

TBD


### -param lpolestream [out]

Pointer to an OLE 1 stream structure where the persistent representation of the object is saved using the OLE 1 storage model.


#### - pStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object to be converted to an OLE 1 storage.


## -returns




						This function supports the standard return value E_INVALIDARG, in addition to the following:




## -remarks



This function converts an OLE 2 storage object to OLE 1 format. The <b>OLESTREAM</b> structure code implemented for OLE 1 must be available.

On entry, the stream to which <i>lpolestm</i> points should be created and positioned just as it would be for an 
<a href="_ole_olesavetostream">OleSaveToStream</a> call. On exit, the stream contains the persistent representation of the object using OLE 1 storage.

<div class="alert"><b>Note</b>  Paintbrush objects are dealt with differently from other objects because their native data is in device-independent bitmap (DIB) format. When Paintbrush objects are converted using 
<b>OleConvertIStorageToOLESTREAM</b>, no presentation data is added to the <b>OLESTREAM</b> structure. To include presentation data, use the 
<a href="https://msdn.microsoft.com/a6026b71-4223-40ab-b209-44531480db57">OleConvertIStorageToOLESTREAMEx</a> function instead.</div>
<div> </div>



## -see-also




<a href="_com_coisole1class">CoIsOle1Class</a>



<a href="https://msdn.microsoft.com/a6026b71-4223-40ab-b209-44531480db57">OleConvertIStorageToOLESTREAMEx</a>



<a href="https://msdn.microsoft.com/8fed879c-5f97-4450-8259-da9643dd828c">OleConvertOLESTREAMToIStorage</a>



<a href="https://msdn.microsoft.com/2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f">OleConvertOLESTREAMToIStorageEx</a>
 

 

