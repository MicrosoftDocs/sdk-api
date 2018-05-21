---
UID: NF:tom.ITextRange.GetStart
title: ITextRange::GetStart
author: windows-driver-content
description: Gets the start character position of the range.
old-location: controls\ITextRange_GetStart.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstart.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetStart, GetStart method [Windows Controls], GetStart method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetStart method, ITextRange.GetStart, ITextRange::GetStart, _win32_ITextRange_GetStart, _win32_ITextRange_GetStart_cpp, controls.ITextRange_GetStart, controls._win32_ITextRange_GetStart, tom/ITextRange::GetStart
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.GetStart
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetStart


## -description


Gets the start character position of the range.


## -parameters




### -param pcpFirst

Type: <b>long*</b>

The start character position. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pcpFirst</i> is null, the method fails and it returns E_INVALIDARG.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/eed9c5f1-416d-4604-8a69-50b284454bb0">GetEnd</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/146c335e-de5a-4418-a0af-51febde720eb">SetStart</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

