---
UID: NF:tom.ITextDocument.Unfreeze
title: ITextDocument::Unfreeze
author: windows-sdk-content
description: Decrements the freeze count.
old-location: controls\ITextDocument_Unfreeze.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\unfreeze.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextDocument interface [Windows Controls],Unfreeze method, ITextDocument.Unfreeze, ITextDocument::Unfreeze, Unfreeze, Unfreeze method [Windows Controls], Unfreeze method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Unfreeze, _win32_ITextDocument_Unfreeze_cpp, controls.ITextDocument_Unfreeze, controls._win32_ITextDocument_Unfreeze, tom/ITextDocument::Unfreeze
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
 - ITextDocument.Unfreeze
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
- ITextDocument.Unfreeze
: 
---

# ITextDocument::Unfreeze


## -description


Decrements the freeze count. 


## -parameters




### -param pCount

Type: <b>long*</b>

The updated freeze count.


## -returns



Type: <b>HRESULT</b>

If the
						freeze count is zero, the method returns <b>S_OK</b>. If the method fails, it returns <b>S_FALSE</b>, indicating that the 
						freeze count is nonzero. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



If the freeze count goes to zero, screen updating is enabled. This method cannot decrement the count below zero, and no error occurs if it is executed with a zero freeze count.

Note, if edit collection is active, screen updating is suppressed, even if the freeze count is zero.




## -see-also




<a href="https://msdn.microsoft.com/145cdaa0-b800-47da-a964-712e80287a3b">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/39ddce52-589e-4dc4-a55c-48902c2fa51e">Freeze</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

