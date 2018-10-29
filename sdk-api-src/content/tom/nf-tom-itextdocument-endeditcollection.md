---
UID: NF:tom.ITextDocument.EndEditCollection
title: ITextDocument::EndEditCollection
author: windows-sdk-content
description: Turns off edit collection (also called undo grouping).
old-location: controls\ITextDocument_EndEditCollection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\endeditcollection.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EndEditCollection, EndEditCollection method [Windows Controls], EndEditCollection method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],EndEditCollection method, ITextDocument.EndEditCollection, ITextDocument::EndEditCollection, _win32_ITextDocument_EndEditCollection, _win32_ITextDocument_EndEditCollection_cpp, controls.ITextDocument_EndEditCollection, controls._win32_ITextDocument_EndEditCollection, tom/ITextDocument::EndEditCollection
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
 - ITextDocument.EndEditCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/145cdaa0-b800-47da-a964-712e80287a3b">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/39ddce52-589e-4dc4-a55c-48902c2fa51e">Freeze</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

