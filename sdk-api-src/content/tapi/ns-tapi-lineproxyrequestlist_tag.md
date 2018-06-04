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

# lineproxyrequestlist_tag structure


## -description


The 
<b>LINEPROXYREQUESTLIST</b> structure describes a list of proxy requests. The 
<a href="https://msdn.microsoft.com/0684f52f-13dd-4734-9242-acd03f7a25ae">lineGetProxyStatus</a> function returns the 
<b>LINEPROXYREQUESTLIST</b> structure.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwNumEntries

Number of <b>DWORD</b> elements that appear in the list array.


### -field dwListSize

Size of the proxy request type list, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of <b>DWORD</b> elements indicating the currently supported proxy request types. Each element is one of the 
<a href="https://msdn.microsoft.com/5c05a567-cc65-411e-b049-919a442c5c57">LINEPROXYREQUEST_ constants</a>. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(DWORD). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/5c05a567-cc65-411e-b049-919a442c5c57">LINEPROXYREQUEST_ Constants</a>



<a href="https://msdn.microsoft.com/0684f52f-13dd-4734-9242-acd03f7a25ae">lineGetProxyStatus</a>
 

 

