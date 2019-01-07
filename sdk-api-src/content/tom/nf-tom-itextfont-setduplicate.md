---
UID: NF:tom.ITextFont.SetDuplicate
title: ITextFont::SetDuplicate
author: windows-sdk-content
description: Sets the character formatting by copying another text font object.
old-location: controls\ITextFont_SetDuplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontsetduplicate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextFont interface [Windows Controls],SetDuplicate method, ITextFont.SetDuplicate, ITextFont::SetDuplicate, SetDuplicate, SetDuplicate method [Windows Controls], SetDuplicate method [Windows Controls],ITextFont interface, _win32_ITextFont_SetDuplicate, _win32_ITextFont_SetDuplicate_cpp, controls.ITextFont_SetDuplicate, controls._win32_ITextFont_SetDuplicate, tom/ITextFont::SetDuplicate
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextFont.SetDuplicate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::SetDuplicate


## -description


Sets the character formatting by copying another text font object. 


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>*</b>

The text font object to apply to this font object. 


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
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

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



Values with the <b>tomUndefined</b> attribute have no effect.

For an example of how to use font duplicates, see <a href="https://msdn.microsoft.com/en-us/library/Bb774145(v=VS.85).aspx">SetFont</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787857(v=VS.85).aspx">GetDuplicate</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774145(v=VS.85).aspx">SetFont</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

