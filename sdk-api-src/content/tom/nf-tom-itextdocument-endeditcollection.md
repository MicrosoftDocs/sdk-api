---
UID: NF:tom.ITextDocument.EndEditCollection
title: ITextDocument::EndEditCollection
author: windows-sdk-content
description: Turns off edit collection (also called undo grouping).
old-location: controls\ITextDocument_EndEditCollection.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\endeditcollection.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: EndEditCollection, EndEditCollection method [Windows Controls], EndEditCollection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],EndEditCollection method, ITextDocument.EndEditCollection, ITextDocument::EndEditCollection, _win32_ITextDocument_EndEditCollection, _win32_ITextDocument_EndEditCollection_cpp, controls.ITextDocument_EndEditCollection, controls._win32_ITextDocument_EndEditCollection, tom/ITextDocument::EndEditCollection
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
 - ITextDocument.EndEditCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::EndEditCollection


## -description


Turns off edit collection (also called <i>undo grouping</i>). 


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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



The screen is unfrozen unless the freeze count is nonzero.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb787730(v=VS.85).aspx">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb773925(v=VS.85).aspx">Freeze</a>



<a href="https://msdn.microsoft.com/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

