---
UID: NF:tom.ITextFont.GetSpacing
title: ITextFont::GetSpacing
author: windows-sdk-content
description: Gets the amount of horizontal spacing between characters.
old-location: controls\ITextFont_GetSpacing.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getspacing.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetSpacing, GetSpacing method [Windows Controls], GetSpacing method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetSpacing method, ITextFont.GetSpacing, ITextFont::GetSpacing, _win32_ITextFont_GetSpacing, _win32_ITextFont_GetSpacing_cpp, controls.ITextFont_GetSpacing, controls._win32_ITextFont_GetSpacing, tom/ITextFont::GetSpacing
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
 - ITextFont.GetSpacing
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetSpacing


## -description


Gets the amount of horizontal spacing between characters.


## -parameters




### -param pValue

Type: <b>float*</b>

The amount of horizontal spacing between characters, in floating-point points. 


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



Displayed text typically has an intercharacter spacing value of zero. Positive values expand the spacing, and negative values compress it.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/4a1ba236-3696-4a68-80bf-30e6a9b53437">SetSpacing</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

