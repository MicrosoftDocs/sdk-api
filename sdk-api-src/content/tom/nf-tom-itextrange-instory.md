---
UID: NF:tom.ITextRange.InStory
title: ITextRange::InStory
author: windows-sdk-content
description: Determines whether this range's story is the same as a specified range's story.
old-location: controls\ITextRange_InStory.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\instory.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextRange interface [Windows Controls],InStory method, ITextRange.InStory, ITextRange::InStory, InStory, InStory method [Windows Controls], InStory method [Windows Controls],ITextRange interface, _win32_ITextRange_InStory, _win32_ITextRange_InStory_cpp, controls.ITextRange_InStory, controls._win32_ITextRange_InStory, tom/ITextRange::InStory
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
 - ITextRange.InStory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::InStory


## -description


Determines whether this range's story is the same as a specified range's story. 


## -parameters




### -param pRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>*</b>

The <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> object whose story is compared to this range's story. 


### -param pValue

TBD




#### - pB

Type: <b>long*</b>

The comparison result. The pointer can be null. The <i>pB</i> parameter receives <b>tomTrue</b> if this range's story is the same as that of the <i>pRange</i>; otherwise it receives <b>tomFalse</b>. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the two stories are the same, the method returns <b>S_OK</b>. Otherwise, it returns S_FALSE.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

