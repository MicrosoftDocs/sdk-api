---
UID: NF:tom.ITextRange2.SetFont2
title: ITextRange2::SetFont2 (tom.h)
author: windows-sdk-content
description: Sets the character formatting attributes of the range.
old-location: controls\itextrange2_setfont2.htm
tech.root: Controls
ms.assetid: ff3c2bf3-efb8-454e-b0e2-e65afeb1a091
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetFont2 method, ITextRange2.SetFont2, ITextRange2::SetFont2, SetFont2, SetFont2 method [Windows Controls], SetFont2 method [Windows Controls],ITextRange2 interface, controls.itextrange2_setfont2, tom/ITextRange2::SetFont2
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.SetFont2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::SetFont2


## -description


Sets the character formatting attributes of the range.


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>*</b>

The font object with the desired character formatting attributes.


## -returns



Type: <b>HRESULT</b>

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
 




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/24ef7fb3-4cf4-46ed-9273-6f91c77f7641">ITextRange2::GetFont2</a>
 

 

