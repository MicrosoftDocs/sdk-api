---
UID: NF:sbe.ISBE2EnumStream.Skip
title: ISBE2EnumStream::Skip
author: windows-sdk-content
description: Skips a specified number of streams in the enumeration sequence.
old-location: mstv\isbe2enumstream_skip.htm
old-project: mstv
ms.assetid: 52979cbc-203b-49ae-9892-db1abfeae94b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ISBE2EnumStream interface [Microsoft TV Technologies],Skip method, ISBE2EnumStream.Skip, ISBE2EnumStream::Skip, Skip, Skip method [Microsoft TV Technologies], Skip method [Microsoft TV Technologies],ISBE2EnumStream interface, mstv.isbe2enumstream_skip, sbe/ISBE2EnumStream::Skip
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
 - ISBE2EnumStream.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISBE2EnumStream::Skip


## -description



      Skips a specified number of streams in the enumeration sequence.


## -parameters




### -param cRecords [in]

The number of streams to skip.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The end of the sequence was reached before skipping the requested number of streams.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/77a918f8-d305-4d4d-9a5c-523ddb796b26">ISBE2EnumStream</a>
 

 

