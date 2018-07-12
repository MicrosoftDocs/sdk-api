---
UID: NF:micaut.IMathInputControl.SetOwnerWindow
title: IMathInputControl::SetOwnerWindow
author: windows-sdk-content
description: Modifies the window that owns this control.
old-location: tablet\imathinputcontrol_setownerwindow.htm
old-project: tablet
ms.assetid: 2f92f731-3297-4da3-a2b9-18e1583c8b1d
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetOwnerWindow method, IMathInputControl.SetOwnerWindow, IMathInputControl::SetOwnerWindow, SetOwnerWindow, SetOwnerWindow method [Tablet PC], SetOwnerWindow method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetOwnerWindow, tablet.imathinputcontrol_setownerwindow
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.SetOwnerWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::SetOwnerWindow


## -description


Modifies the window that owns this control.


## -parameters




### -param OwnerWindow [in]

A handle to the owner window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The math input control always appears on top of the window that owns it.




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

