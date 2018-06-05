---
UID: NF:tom.ITextDocument.Save
title: ITextDocument::Save
author: windows-sdk-content
description: Saves the document.
old-location: controls\ITextDocument_Save.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\save.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextDocument interface [Windows Controls],Save method, ITextDocument.Save, ITextDocument::Save, Save, Save method [Windows Controls], Save method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Save, _win32_ITextDocument_Save_cpp, controls.ITextDocument_Save, controls._win32_ITextDocument_Save, tom/ITextDocument::Save
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::Save


## -description


Saves the document. 


## -parameters




### -param pVar [in]

Type: <b>VARIANT*</b>

The save target. This parameter is a <b>VARIANT</b>, which can be a file name, or <b>NULL</b>. 


### -param Flags [in]

Type: <b>long</b>

File creation, open, share, and conversion flags. For a list of possible values, see <a href="https://msdn.microsoft.com/6ea20837-4987-49c9-88e5-81d79c9016ac">ITextDocument::Open</a>. 


### -param CodePage [in]

Type: <b>long</b>

The specified code page. Common values are CP_ACP (zero: system ANSI code page), 1200 (Unicode), and 1208 (UTF-8). 


## -returns



Type: <b>HRESULT</b>

The return value can be an 
						<b>HRESULT</b> value that corresponds to a system error code or a COM error code, including one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeds.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Feature not implemented.

</td>
</tr>
</table>
 




## -remarks



To use the parameters that were specified for opening the file, use zero values for the parameters. 

If 
				<i>pVar</i> is null or missing, the file name given by this document's name is used. If both of these are missing or null, the method fails. 

If 
				<i>pVar</i> specifies a file name, that name should replace the current Name property. Similarly, the 
				<i>Flags</i> and 
				<i>CodePage</i> arguments can overrule those supplied in the 
				<a href="https://msdn.microsoft.com/6ea20837-4987-49c9-88e5-81d79c9016ac">ITextDocument::Open</a> method and define the values to use for files created with the 
				<a href="https://msdn.microsoft.com/69f90d70-dac6-4f20-91e5-858fe9253c50">ITextDocument::New</a> method.

Unicode plain-text files should be saved with the Unicode byte-order mark (0xFEFF) as the first character. This character should be removed when the file is read in; that is, it is only used for import/export to identify the plain text as Unicode and to identify the byte order of that text. Microsoft Notepad adopted this convention, which is now recommended by the Unicode standard.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/69f90d70-dac6-4f20-91e5-858fe9253c50">New</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

