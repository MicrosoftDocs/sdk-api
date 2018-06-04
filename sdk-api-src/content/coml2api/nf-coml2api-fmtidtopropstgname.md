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

# FmtIdToPropStgName function


## -description


The <b>FmtIdToPropStgName</b> function converts a property set format identifier (FMTID) to its storage or stream name.


## -parameters




### -param pfmtid [in]

A pointer to the FMTID of the property set.


### -param oszName [out]

A pointer to a null-terminated string that receives the storage or stream name of the property set identified by <i>pfmtid</i>. The array allocated for this string must be at least CCH_MAX_PROPSTG_NAME (32) characters in length.


## -returns




						This function supports the standard return value E_INVALIDARG as well as the following:




## -remarks



<b>FmtIdToPropStgName</b> maps a property set FMTID to its stream name for a simple property set or to its storage name for a nonsimple property set.

This function is useful in creating or opening a property set using the PROPSETFLAG_UNBUFFERED value with the 
<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a> and 
<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/bbbaf5a3-df17-42fd-ba2b-ad5b572c8a3f">PropStgNameToFmtId</a>



<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a>



<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a>
 

 

