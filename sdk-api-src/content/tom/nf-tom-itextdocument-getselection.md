---
UID: NF:tom.ITextDocument.GetSelection
title: ITextDocument::GetSelection
author: windows-sdk-content
description: Gets the active selection.
old-location: controls\ITextDocument_GetSelection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getselection.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSelection, GetSelection method [Windows Controls], GetSelection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetSelection method, ITextDocument.GetSelection, ITextDocument::GetSelection, _win32_ITextDocument_GetSelection, _win32_ITextDocument_GetSelection_cpp, controls.ITextDocument_GetSelection, controls._win32_ITextDocument_GetSelection, tom/ITextDocument::GetSelection
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
 - ITextDocument.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::GetSelection


## -description


Gets the active selection.


## -parameters




### -param ppSel

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774060(v=VS.85).aspx">ITextSelection</a>**</b>

The active selection. 


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates no active selection.

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
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774060(v=VS.85).aspx">ITextSelection</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

