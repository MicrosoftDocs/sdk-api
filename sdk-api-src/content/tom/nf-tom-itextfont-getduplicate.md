---
UID: NF:tom.ITextFont.GetDuplicate
title: ITextFont::GetDuplicate
author: windows-sdk-content
description: Gets a duplicate of this text font object.
old-location: controls\ITextFont_GetDuplicate.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontgetduplicate.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetDuplicate, GetDuplicate method [Windows Controls], GetDuplicate method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetDuplicate method, ITextFont.GetDuplicate, ITextFont::GetDuplicate, _win32_ITextFont_GetDuplicate, _win32_ITextFont_GetDuplicate_cpp, controls.ITextFont_GetDuplicate, controls._win32_ITextFont_GetDuplicate, tom/ITextFont::GetDuplicate
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
 - ITextFont.GetDuplicate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::GetDuplicate


## -description


Gets a duplicate of this text font object. 


## -parameters




### -param ppFont

Type: <b><a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>**</b>

The duplicate text font object. 


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the new object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method includes an invalid argument.

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



The duplicate property is the default property of an <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> object.

For an example of how to use font duplicates, see <a href="https://msdn.microsoft.com/15630fec-83b2-4169-b141-8ce253dd25fe">SetFont</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/eb71e34a-adf9-4700-b6f0-42f8b1c30881">SetDuplicate</a>



<a href="https://msdn.microsoft.com/15630fec-83b2-4169-b141-8ce253dd25fe">SetFont</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

