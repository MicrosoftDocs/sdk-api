---
UID: NF:tom.ITextRange2.SetFormattedText2
title: ITextRange2::SetFormattedText2
author: windows-sdk-content
description: Sets the text of this range to the formatted text of the specified range.
old-location: controls\itextrange2_setformattedtext2.htm
tech.root: controls
ms.assetid: 151be9ee-da5d-4e50-a12e-0473cf1c7d91
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextRange2 interface [Windows Controls],SetFormattedText2 method, ITextRange2.SetFormattedText2, ITextRange2::SetFormattedText2, SetFormattedText2, SetFormattedText2 method [Windows Controls], SetFormattedText2 method [Windows Controls],ITextRange2 interface, controls.itextrange2_setformattedtext2, tom/ITextRange2::SetFormattedText2
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
 - ITextRange2.SetFormattedText2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextRange2.SetFormattedText2
: 
---

# ITextRange2::SetFormattedText2


## -description


Sets the text of this range to the formatted text of the specified range. 


## -parameters




### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>*</b>

The range that contains the formatted text that replaces the text of this range.


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



<a href="https://msdn.microsoft.com/9fe5d82d-b13e-4b94-beb6-15691d4c5176">ITextRange2::GetFormattedText2</a>
 

 

