---
UID: NF:tom.ITextStory.GetRange
title: ITextStory::GetRange
author: windows-sdk-content
description: Gets a text range object for the story.
old-location: controls\itextstory_getrange.htm
old-project: Controls
ms.assetid: 7cc02056-c431-470a-83ef-99e47123da1e
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetRange, GetRange method [Windows Controls], GetRange method [Windows Controls],ITextStory interface, ITextStory interface [Windows Controls],GetRange method, ITextStory.GetRange, ITextStory::GetRange, controls.itextstory_getrange, tom/ITextStory::GetRange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory.GetRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory::GetRange


## -description


Gets a text range object for the story.


## -parameters




### -param cpActive [in]

Type: <b>long</b>

The active end of the range.


### -param cpAnchor [in]

Type: <b>long</b>

The anchor end of the range.


### -param ppRange [out, retval]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>**</b>

The text range object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>
 

 

