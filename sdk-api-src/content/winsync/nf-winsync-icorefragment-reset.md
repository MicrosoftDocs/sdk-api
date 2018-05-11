---
UID: NF:winsync.ICoreFragment.Reset
title: ICoreFragment::Reset
author: windows-driver-content
description: Resets both the column and range enumerators to the beginning of their respective sets.
old-location: winsync\icorefragment_reset.htm
old-project: winsync
ms.assetid: b39e9dee-7437-4480-9050-33bc68b41b00
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICoreFragment interface [Windows Sync],Reset method, ICoreFragment.Reset, ICoreFragment::Reset, Reset, Reset method [Windows Sync], Reset method [Windows Sync],ICoreFragment interface, winsync.icorefragment_reset, winsync/ICoreFragment::Reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ICoreFragment.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ICoreFragment::Reset


## -description


Resets both the column and range enumerators to the beginning of their respective sets.


## -parameters






## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object contained in this object has changed since this object was created.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3e232531-ad44-4ad1-b186-46edbc07291b">ICoreFragment Interface</a>
 

 

