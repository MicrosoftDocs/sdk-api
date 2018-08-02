---
UID: NF:tom.ITextStory.SetFormattedText
title: ITextStory::SetFormattedText
author: windows-sdk-content
description: Replaces a story’s text with specified formatted text.
old-location: controls\itextstory_setformattedtext.htm
old-project: Controls
ms.assetid: ddc77bfe-06de-43e6-9d74-f1b3531c9416
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextStory interface [Windows Controls],SetFormattedText method, ITextStory.SetFormattedText, ITextStory::SetFormattedText, SetFormattedText, SetFormattedText method [Windows Controls], SetFormattedText method [Windows Controls],ITextStory interface, controls.itextstory_setformattedtext, tom/ITextStory::SetFormattedText
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
 - ITextStory.SetFormattedText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory::SetFormattedText


## -description


Replaces a story’s text with specified formatted text.


## -parameters




### -param pUnk [in]

Type: <b>IUnknown*</b>

The formatted text to replace the story’s text.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

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
 




## -remarks



This method calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> for an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>
 

 

