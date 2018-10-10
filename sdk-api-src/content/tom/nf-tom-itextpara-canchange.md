---
UID: NF:tom.ITextPara.CanChange
title: ITextPara::CanChange
author: windows-sdk-content
description: Determines whether the paragraph formatting can be changed.
old-location: controls\ITextPara_CanChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparacanchange.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CanChange, CanChange method [Windows Controls], CanChange method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],CanChange method, ITextPara.CanChange, ITextPara::CanChange, _win32_ITextPara_CanChange, _win32_ITextPara_CanChange_cpp, controls.ITextPara_CanChange, controls._win32_ITextPara_CanChange, tom/ITextPara::CanChange
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
 - ITextPara.CanChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::CanChange


## -description


Determines whether the paragraph formatting can be changed. 


## -parameters




### -param pValue

TBD




#### - pbCanChange [retval]

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the paragraph formatting can be changed or <b>tomFalse</b> if it cannot be changed. This parameter can be null. 


## -returns



Type: <b>HRESULT</b>

If paragraph formatting can change, <b>ITextPara::CanChange</b> succeeds and returns <b>S_OK</b>. If paragraph formatting cannot change, the method fails and returns S_FALSE. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -remarks



The *<i>pbCanChange</i>  parameter returns <b>tomTrue</b> only if the paragraph formatting can be changed (that is, if no part of an associated range is protected and an associated document is not read-only). If this <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> object is a duplicate, no protection rules apply.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

