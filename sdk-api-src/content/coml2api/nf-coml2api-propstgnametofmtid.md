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

# PropStgNameToFmtId function


## -description



			The <b>PropStgNameToFmtId</b> function converts a property set storage or stream name to its format identifier.


## -parameters




### -param oszName [in]

A pointer to a null-terminated Unicode string that contains the stream name of a simple property set or the storage name of a nonsimple property set.


### -param pfmtid [out]

A pointer to a FMTID variable that receives the format identifier of the property set specified by <i>oszName</i>.


## -returns




						This function supports the standard return value E_INVALIDARG as well as the following:




## -remarks



The <b>PropStgNameToFmtId</b> function maps the stream name of a simple property set or the storage name of a nonsimple property set to its format identifier.

This function is useful in creating or opening a property set using the PROPSETFLAG_UNBUFFERED value with the 
<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a> and 
<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/044f8883-bbd2-4cd3-b9dc-739ecb711bdd">FmtIdToPropStgName</a>



<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a>



<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a>
 

 

