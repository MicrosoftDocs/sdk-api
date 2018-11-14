---
UID: NF:tom.ITextDocument.BeginEditCollection
title: ITextDocument::BeginEditCollection
author: windows-sdk-content
description: Turns on edit collection (also called undo grouping).
old-location: controls\ITextDocument_BeginEditCollection.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\begineditcollection.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: BeginEditCollection, BeginEditCollection method [Windows Controls], BeginEditCollection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],BeginEditCollection method, ITextDocument.BeginEditCollection, ITextDocument::BeginEditCollection, _win32_ITextDocument_BeginEditCollection, _win32_ITextDocument_BeginEditCollection_cpp, controls.ITextDocument_BeginEditCollection, controls._win32_ITextDocument_BeginEditCollection, tom/ITextDocument::BeginEditCollection
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
 - ITextDocument.BeginEditCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextDocument.BeginEditCollection
: 
---

# ITextDocument::BeginEditCollection


## -description


Turns on edit collection (also called <i>undo grouping</i>). 


## -parameters






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
Undo is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
 




## -remarks



A single 
				<b>Undo</b> command undoes all changes made while edit collection is turned on.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787750(v=VS.85).aspx">EndEditCollection</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773925(v=VS.85).aspx">Freeze</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

