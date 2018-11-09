---
UID: NF:tom.ITextPara.GetFirstLineIndent
title: ITextPara::GetFirstLineIndent
author: windows-sdk-content
description: Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.
old-location: controls\ITextPara_GetFirstLineIndent.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getfirstlineindent.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetFirstLineIndent, GetFirstLineIndent method [Windows Controls], GetFirstLineIndent method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetFirstLineIndent method, ITextPara.GetFirstLineIndent, ITextPara::GetFirstLineIndent, _win32_ITextPara_GetFirstLineIndent, _win32_ITextPara_GetFirstLineIndent_cpp, controls.ITextPara_GetFirstLineIndent, controls._win32_ITextPara_GetFirstLineIndent, tom/ITextPara::GetFirstLineIndent
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
 - ITextPara.GetFirstLineIndent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetFirstLineIndent


## -description


Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.


## -parameters




### -param pValue

Type: <b>float*</b>

The first-line indentation amount in floating-point points.


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetFirstLineIndent</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
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
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -remarks



To set the first line indentation amount, call the <a href="https://msdn.microsoft.com/en-us/library/Bb774155(v=VS.85).aspx">ITextPara::SetIndents</a> method.

To get and set the indent for all other lines of the paragraph (that is, the left
				indent), use <a href="https://msdn.microsoft.com/en-us/library/Bb773977(v=VS.85).aspx">ITextPara::GetLeftIndent</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774155(v=VS.85).aspx">ITextPara::SetIndents</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb773977(v=VS.85).aspx">GetLeftIndent</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774155(v=VS.85).aspx">SetIndents</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

