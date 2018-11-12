---
UID: NS:tapi.lineproxyrequestlist_tag
title: lineproxyrequestlist_tag
author: windows-sdk-content
description: The LINEPROXYREQUESTLIST structure describes a list of proxy requests. The lineGetProxyStatus function returns the LINEPROXYREQUESTLIST structure.
old-location: tapi2\lineproxyrequestlist.htm
tech.root: tapi
ms.assetid: dc417954-56b4-4436-9582-7b656121fd6f
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*LPLINEPROXYREQUESTLIST, LINEPROXYREQUESTLIST, LINEPROXYREQUESTLIST structure [TAPI 2.2], LPLINEPROXYREQUESTLIST, LPLINEPROXYREQUESTLIST structure pointer [TAPI 2.2], _tapi2_lineproxyrequestlist, lineproxyrequestlist_tag, tapi/LINEPROXYREQUESTLIST, tapi/LPLINEPROXYREQUESTLIST, tapi2.lineproxyrequestlist"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEPROXYREQUESTLIST
product: Windows
targetos: Windows
req.typenames: LINEPROXYREQUESTLIST, *LPLINEPROXYREQUESTLIST
req.redist: 
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
 

 

