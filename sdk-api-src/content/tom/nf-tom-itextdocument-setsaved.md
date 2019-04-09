---
UID: NF:tom.ITextDocument.SetSaved
title: ITextDocument::SetSaved (tom.h)
author: windows-sdk-content
description: Sets the document Saved property.
old-location: controls\ITextDocument_SetSaved.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setsaved.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],SetSaved method, ITextDocument.SetSaved, ITextDocument::SetSaved, SetSaved, SetSaved method [Windows Controls], SetSaved method [Windows Controls],ITextDocument interface, _win32_ITextDocument_SetSaved, _win32_ITextDocument_SetSaved_cpp, controls.ITextDocument_SetSaved, controls._win32_ITextDocument_SetSaved, tom/ITextDocument::SetSaved, tomFalse, tomTrue
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
 - ITextDocument.SetSaved
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::SetSaved


## -description


Sets the document 
			<b>Saved</b> property.


## -parameters




### -param Value [in]

Type: <b>long</b>

New value of the 
					<b>Saved</b> property. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomTrue"></a><a id="tomtrue"></a><a id="TOMTRUE"></a><dl>
<dt><b>tomTrue</b></dt>
</dl>
</td>
<td width="60%">
No changes to the file since the last time it was saved.

</td>
</tr>
<tr>
<td width="40%"><a id="tomFalse"></a><a id="tomfalse"></a><a id="TOMFALSE"></a><dl>
<dt><b>tomFalse</b></dt>
</dl>
</td>
<td width="60%">
There are changes to the file.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

The return value is <b>S_OK</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774011(v=VS.85).aspx">GetSaved</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

