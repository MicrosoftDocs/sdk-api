---
UID: NF:tom.ITextDocument.Unfreeze
title: ITextDocument::Unfreeze (tom.h)
author: windows-sdk-content
description: Decrements the freeze count.
old-location: controls\ITextDocument_Unfreeze.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\unfreeze.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],Unfreeze method, ITextDocument.Unfreeze, ITextDocument::Unfreeze, Unfreeze, Unfreeze method [Windows Controls], Unfreeze method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Unfreeze, _win32_ITextDocument_Unfreeze_cpp, controls.ITextDocument_Unfreeze, controls._win32_ITextDocument_Unfreeze, tom/ITextDocument::Unfreeze
ms.topic: method
f1_keywords: 
 - "tom/ITextDocument.Unfreeze"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
						freeze count is nonzero. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.




## -remarks



If the freeze count goes to zero, screen updating is enabled. This method cannot decrement the count below zero, and no error occurs if it is executed with a zero freeze count.

Note, if edit collection is active, screen updating is suppressed, even if the freeze count is zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-begineditcollection">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-freeze">Freeze</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

