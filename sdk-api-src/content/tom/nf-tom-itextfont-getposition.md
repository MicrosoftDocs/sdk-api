---
UID: NF:tom.ITextFont.GetPosition
title: ITextFont::GetPosition
author: windows-sdk-content
description: Gets the amount that characters are offset vertically relative to the baseline.
old-location: controls\ITextFont_GetPosition.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getposition.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetPosition, GetPosition method [Windows Controls], GetPosition method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetPosition method, ITextFont.GetPosition, ITextFont::GetPosition, _win32_ITextFont_GetPosition, _win32_ITextFont_GetPosition_cpp, controls.ITextFont_GetPosition, controls._win32_ITextFont_GetPosition, tom/ITextFont::GetPosition
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
 - ITextFont.GetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetPosition


## -description


Gets the amount that characters are  offset vertically relative to the baseline.


## -parameters




### -param pValue

Type: <b>float*</b>

The amount of vertical offset, in floating-point points. 


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
 




## -remarks



Displayed text typically has a zero value for this property. Positive values raise the text, and negative values lower it.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787801(v=VS.85).aspx">SetPosition</a>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

