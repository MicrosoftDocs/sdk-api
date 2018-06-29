---
UID: NF:tom.ITextFont.SetPosition
title: ITextFont::SetPosition
author: windows-sdk-content
description: Sets the amount that characters are offset vertically relative to the baseline.
old-location: controls\ITextFont_SetPosition.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setposition.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextFont interface [Windows Controls],SetPosition method, ITextFont.SetPosition, ITextFont::SetPosition, SetPosition, SetPosition method [Windows Controls], SetPosition method [Windows Controls],ITextFont interface, _win32_ITextFont_SetPosition, _win32_ITextFont_SetPosition_cpp, controls.ITextFont_SetPosition, controls._win32_ITextFont_SetPosition, tom/ITextFont::SetPosition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont.SetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::SetPosition


## -description


Sets the amount that characters are  offset vertically relative to the baseline.


## -parameters




### -param Value [in]

Type: <b>float</b>

 The new amount of vertical offset, in floating-point points. 


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



Displayed text typically has a zero value for this property. Positive values raise the text, and negative values lower it.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774005(v=VS.85).aspx">GetPosition</a>



<a href="https://msdn.microsoft.com/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

