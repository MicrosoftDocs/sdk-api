---
UID: NF:tom.ITextPara.IsEqual
title: ITextPara::IsEqual
author: windows-sdk-content
description: Determines if the current range has the same properties as a specified range.
old-location: controls\ITextPara_IsEqual.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparaisequal.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ITextPara interface [Windows Controls],IsEqual method, ITextPara.IsEqual, ITextPara::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextPara interface, _win32_ITextPara_IsEqual, _win32_ITextPara_IsEqual_cpp, controls.ITextPara_IsEqual, controls._win32_ITextPara_IsEqual, tom/ITextPara::IsEqual
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
 - ITextPara.IsEqual
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::IsEqual


## -description


Determines if the current range has the same properties as a specified range.


## -parameters




### -param pPara

Type: <b><a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>*</b>

The <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> range that is compared to the current range. 


### -param pValue






#### - pB

Type: <b>long*</b>

The comparison result. The value can be null. 


## -returns



Type: <b>HRESULT</b>

If the objects are equal, <b>ITextPara::IsEqual</b> succeeds and returns <b>S_OK</b>. If the objects are not equal, the method fails and returns S_FALSE. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

