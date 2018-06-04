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

# OleConvertIStorageToOLESTREAMEx function


## -description



			The 
<b>OleConvertIStorageToOLESTREAMEx</b> function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model, including the presentation data. This is one of several functions included in Structured Storage to ensure compatibility between OLE1 and OLE2.


## -parameters




### -param pstg

TBD


### -param cfFormat [in]

Format of the presentation data. May be <b>NULL</b>, in which case the <i>lWidth</i>, <i>lHeight</i>, <i>dwSize</i>, and <i>pmedium</i> parameters are ignored.


### -param lWidth [in]

Width of the object presentation data in HIMETRIC units.


### -param lHeight [in]

Height of the object presentation data in HIMETRIC units.


### -param dwSize [in]

Size of the data, in bytes, to be converted.


### -param pmedium [in]

Pointer to the 
<a href="_ole_stgmedium">STGMEDIUM</a> structure for the serialized data to be converted.


### -param polestm

TBD




#### - lpolestm [out]

Pointer to a stream where the persistent representation of the object is saved using the OLE 1 storage model.


#### - pStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object to be converted to an OLE 1 storage.


## -returns




						This function supports the standard return value E_INVALIDARG, in addition to the following:




## -remarks



The 
<b>OleConvertIStorageToOLESTREAMEx</b> function converts an OLE 2 storage object to OLE 1 format. It differs from the 
<a href="https://msdn.microsoft.com/d100d32a-6559-4a7c-a0ae-780bc9d82611">OleConvertIStorageToOLESTREAM</a> function in that the 
<b>OleConvertIStorageToOLESTREAMEx</b> function also passes the presentation data to the OLE 1 storage object, whereas the 
<b>OleConvertIStorageToOLESTREAM</b> function does not.

Because 
<b>OleConvertIStorageToOLESTREAMEx</b> can specify which presentation data to convert, it can be used by applications that do not use OLE default caching resources but do use OLE's conversion resources.

The value of the <b>tymed</b> member of 
<a href="_ole_stgmedium">STGMEDIUM</a> must be either TYMED_HGLOBAL or TYMED_ISTREAM; refer to the 
<a href="_ole_tymed">TYMED</a> enumeration for more information. The medium is not released by the 
<b>OleConvertIStorageToOLESTREAMEx</b> function.




## -see-also




<a href="_com_coisole1class">CoIsOle1Class</a>



<a href="https://msdn.microsoft.com/d100d32a-6559-4a7c-a0ae-780bc9d82611">OleConvertIStorageToOLESTREAM</a>



<a href="https://msdn.microsoft.com/8fed879c-5f97-4450-8259-da9643dd828c">OleConvertOLESTREAMToIStorage</a>



<a href="https://msdn.microsoft.com/2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f">OleConvertOLESTREAMToIStorageEx</a>



<a href="_ole_stgmedium">STGMEDIUM</a>



<a href="_ole_tymed">TYMED</a>
 

 

