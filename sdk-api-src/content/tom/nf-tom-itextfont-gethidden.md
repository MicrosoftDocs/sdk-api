---
UID: NF:tom.ITextFont.GetHidden
title: ITextFont::GetHidden method
author: windows-driver-content
description: Gets whether characters are hidden.
old-location: controls\ITextFont_GetHidden.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gethidden.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetHidden method [Windows Controls], GetHidden method [Windows Controls], ITextFont interface, GetHidden,ITextFont.GetHidden, ITextFont, ITextFont interface [Windows Controls], GetHidden method, ITextFont::GetHidden, _win32_ITextFont_GetHidden, _win32_ITextFont_GetHidden_cpp, controls.ITextFont_GetHidden, controls._win32_ITextFont_GetHidden, tom/ITextFont::GetHidden
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont.GetHidden
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetHidden method


## -description


Gets whether characters are hidden.


## -parameters




### -param pValue

Type: <b>long*</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are hidden.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not hidden.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Hidden property is undefined.</td>
</tr>
</table>
 


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



This property corresponds to the <b>CFE_HIDDEN</b> effect described in the <a href="https://msdn.microsoft.com/e0057d40-e479-4706-b677-b8fb727a8118">CHARFORMAT2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/e0057d40-e479-4706-b677-b8fb727a8118">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5d655c8b-3686-4c32-84aa-77e4b09e2965">SetHidden</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

