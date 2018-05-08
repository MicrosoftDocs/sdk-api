---
UID: NF:micaut.IMathInputControl.EnableAutoGrow
title: IMathInputControl::EnableAutoGrow
author: windows-driver-content
description: Determines whether the control automatically grows when input is entered beyond the control's current range.
old-location: tablet\imathinputcontrol_enableautogrow.htm
old-project: tablet
ms.assetid: 23eae5ee-8f3d-4f54-9c30-b29f0c14ba7f
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: EnableAutoGrow, EnableAutoGrow method [Tablet PC], EnableAutoGrow method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],EnableAutoGrow method, IMathInputControl.EnableAutoGrow, IMathInputControl::EnableAutoGrow, micaut/IMathInputControl::EnableAutoGrow, tablet.imathinputcontrol_enableautogrow
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
-	IMathInputControl.EnableAutoGrow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::EnableAutoGrow


## -description


Determines whether the control automatically grows when input is entered beyond the control's current range.


## -parameters




### -param AutoGrow [in]

<b>VARIANT_TRUE</b> to enable automatic growth; otherwise, <b>VARIANT_FALSE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Automatic growth is enabled by default.
  




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

