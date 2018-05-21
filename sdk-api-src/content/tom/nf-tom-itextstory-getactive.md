---
UID: NF:tom.ITextStory.GetActive
title: ITextStory::GetActive
author: windows-driver-content
description: Sets the active state of a story.
old-location: controls\itextstory_getactive.htm
old-project: Controls
ms.assetid: 7bae9458-ee68-486a-a37f-2cc899400882
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetActive, GetActive method [Windows Controls], GetActive method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetActive method, ITextStory.GetActive, ITextStory::GetActive, controls.itextstory_getactive, tom/ITextStory::GetActive, tomDisplayActive, tomDisplayUIActive, tomInactive, tomUIActive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tom.h
api_name:
-	ITextStory.GetActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory::GetActive


## -description


Sets the active state of a story.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The active state. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomDisplayActive"></a><a id="tomdisplayactive"></a><a id="TOMDISPLAYACTIVE"></a><dl>
<dt><b>tomDisplayActive</b></dt>
</dl>
</td>
<td width="60%">
The story has no UI or display (fast and lightweight).

</td>
</tr>
<tr>
<td width="40%"><a id="tomDisplayUIActive"></a><a id="tomdisplayuiactive"></a><a id="TOMDISPLAYUIACTIVE"></a><dl>
<dt><b>tomDisplayUIActive</b></dt>
</dl>
</td>
<td width="60%">
The story is UI active; that is, gets keyboard and mouse interactions.

</td>
</tr>
<tr>
<td width="40%"><a id="tomInactive"></a><a id="tominactive"></a><a id="TOMINACTIVE"></a><dl>
<dt><b>tomInactive</b></dt>
</dl>
</td>
<td width="60%">
The story has display, but no UI.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUIActive"></a><a id="tomuiactive"></a><a id="TOMUIACTIVE"></a><dl>
<dt><b>tomUIActive</b></dt>
</dl>
</td>
<td width="60%">
The story has display and UI activity.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>



<a href="https://msdn.microsoft.com/fa0177be-2016-4205-b121-921dbdbf5b71">ITextStory::SetActive</a>
 

 

