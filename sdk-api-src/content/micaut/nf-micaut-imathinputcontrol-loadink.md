---
UID: NF:micaut.IMathInputControl.LoadInk
title: IMathInputControl::LoadInk
author: windows-driver-content
description: Processes ink and triggers recognition.
old-location: tablet\imathinputcontrol_loadink.htm
old-project: tablet
ms.assetid: 3313cb16-3400-48d5-8ba0-b3bd593b37ea
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IMathInputControl interface [Tablet PC],LoadInk method, IMathInputControl.LoadInk, IMathInputControl::LoadInk, LoadInk, LoadInk method [Tablet PC], LoadInk method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::LoadInk, tablet.imathinputcontrol_loadink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	micaut.h
api_name:
-	IMathInputControl.LoadInk
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::LoadInk


## -description


Processes ink and triggers recognition.


## -parameters




### -param Ink [in]

The ink object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method will only work when the control is visible.
When that ink exceeds the control's current size, and automatic growth is enabled, the control tries to accommodate the input. If the control cannot supply enough space, ink is proportionally shrunk to fit the maximum available size.




## -see-also




<a href="https://msdn.microsoft.com/23eae5ee-8f3d-4f54-9c30-b29f0c14ba7f">EnableAutoGrow</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

