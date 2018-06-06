---
UID: NF:sbe.ISBE2EnumStream.Next
title: ISBE2EnumStream::Next
author: windows-sdk-content
description: Retrieves the next n streams in the collection.
old-location: mstv\isbe2enumstream_next.htm
old-project: mstv
ms.assetid: c6445927-d7a7-4f45-a7ff-14484161b731
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISBE2EnumStream interface [Microsoft TV Technologies],Next method, ISBE2EnumStream.Next, ISBE2EnumStream::Next, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],ISBE2EnumStream interface, mstv.isbe2enumstream_next, sbe/ISBE2EnumStream::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2EnumStream.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2EnumStream::Next


## -description



        Retrieves the next <i>n</i> streams in the collection.
      


## -parameters




### -param cRequest [in]

The number of streams to retrieve.




### -param pStreamDesc [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/ab7ccd5b-1ac8-4d33-aea6-49383025270b">SBE2_STREAM_DESC</a> structures, with at least <i>cRequest</i> elements. The method copies up to <i>cRequest</i> elements into the array.


### -param pcReceived [out]

Receives the number of elements returned in the <i>pStreamDesc</i> array. This parameter can be <b>NULL</b> if <i>cRequest</i> is 1.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded and retrieved <i>cRequest</i> elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The method retrieved fewer elements than requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The streams have changed, so the caller must enumerate them again.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>
 

 

