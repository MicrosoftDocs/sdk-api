---
UID: NF:infotech.IITWordWheel.Lookup(LPCVOID,BOOL,LONG)
title: IITWordWheel::Lookup(LPCVOID,BOOL,LONG)
author: windows-sdk-content
description: Looks up an entry and returns contents in a buffer.
old-location: htmlhelp\iitwordwheel_lookup1.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheellookupbuffer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IITWordWheel interface [HTML Help Workshop],Lookup method, IITWordWheel.Lookup, IITWordWheel.Lookup(LPCVOID,BOOL,LONG), IITWordWheel::Lookup, IITWordWheel::Lookup(LONG,LPVOID,DWORD), IITWordWheel::Lookup(LPCVOID,BOOL,LONG), Lookup, Lookup method [HTML Help Workshop], Lookup method [HTML Help Workshop],IITWordWheel interface, htmlhelp.iitwordwheel_lookup1, infotech/IITWordWheel::Lookup, refIITWordWheelLookupBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: infotech.h
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
 - COM
api_location:
 - Infotech.h
api_name:
 - IITWordWheel.Lookup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IITWordWheel::Lookup(LPCVOID,BOOL,LONG)


## -description


Looks up an entry and returns contents in a buffer.




## -parameters




#### - lpcvPrefix [in]

Entry to look up.




#### - fExactMatch [out]

Buffer to return entry.




#### - plEntry [in]

Buffer size in number of bytes.




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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The word wheel entry was successfully returned.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFRANGE</b></dt>
</dl>
</td>
<td width="60%">
Entry number is out of range.



</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9734c73e-9325-4a6d-bbf3-3f87f96a662e">IITWordWheel</a>
 

 

