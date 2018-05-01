---
UID: NF:infotech.IITWordWheel.Lookup
title: IITWordWheel::Lookup method
author: windows-driver-content
description: Looks up an entry and returns contents in a buffer.
old-location: htmlhelp\iitwordwheel_lookup1.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheellookupbuffer.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IITWordWheel, IITWordWheel interface [HTML Help Workshop], Lookup method, IITWordWheel::Lookup, Lookup method [HTML Help Workshop], Lookup method [HTML Help Workshop], IITWordWheel interface, Lookup,IITWordWheel.Lookup, htmlhelp.iitwordwheel_lookup1, infotech/IITWordWheel::Lookup, refIITWordWheelLookupBuffer
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
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITWordWheel.Lookup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITWordWheel::Lookup method


## -description


Looks up an entry and returns contents in a buffer.




## -parameters




### -param lEntry [in]

Entry to look up.




### -param lpvKeyBuf [out]

Buffer to return entry.




### -param cbKeyBuf [in]

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
 

 

