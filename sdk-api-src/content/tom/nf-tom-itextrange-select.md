---
UID: NF:tom.ITextRange.Select
title: ITextRange::Select
author: windows-sdk-content
description: Sets the start and end positions, and story values of the active selection, to those of this range.
old-location: controls\ITextRange_Select.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\select.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRange interface [Windows Controls],Select method, ITextRange.Select, ITextRange::Select, Select, Select method [Windows Controls], Select method [Windows Controls],ITextRange interface, _win32_ITextRange_Select, _win32_ITextRange_Select_cpp, controls.ITextRange_Select, controls._win32_ITextRange_Select, tom/ITextRange::Select
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
 - ITextRange.Select
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::Select


## -description


Sets the start and end positions, and story values of the active selection, to those of this range. 


## -parameters






## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.




## -remarks



The active end of the new selection is at the end position. 

The caret for an ambiguous character position is displayed at the beginning of the line. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

