---
UID: NF:ole2.OleConvertIStorageToOLESTREAM
title: OleConvertIStorageToOLESTREAM function
author: windows-driver-content
description: The OleConvertIStorageToOLESTREAM function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model but does not include the presentation data. This is one of several compatibility functions.
old-location: stg\oleconvertistoragetoolestream.htm
old-project: Stg
ms.assetid: d100d32a-6559-4a7c-a0ae-780bc9d82611
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: OleConvertIStorageToOLESTREAM, OleConvertIStorageToOLESTREAM function [Structured Storage], _stg_oleconvertistoragetoolestream, ole2/OleConvertIStorageToOLESTREAM, stg.oleconvertistoragetoolestream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	OleConvertIStorageToOLESTREAM
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

