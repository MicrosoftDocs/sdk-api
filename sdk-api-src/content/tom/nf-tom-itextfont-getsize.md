---
UID: NF:tom.ITextFont.GetSize
title: ITextFont::GetSize
author: windows-sdk-content
description: Gets the font size.
old-location: controls\ITextFont_GetSize.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getsize.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSize, GetSize method [Windows Controls], GetSize method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetSize method, ITextFont.GetSize, ITextFont::GetSize, _win32_ITextFont_GetSize, _win32_ITextFont_GetSize_cpp, controls.ITextFont_GetSize, controls._win32_ITextFont_GetSize, tom/ITextFont::GetSize
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
 - ITextFont.GetSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::GetSize


## -description


Gets the font size.


## -parameters




### -param pValue

Type: <b>float*</b>

The font size, in floating-point points. 


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
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787813(v=VS.85).aspx">SetSize</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

