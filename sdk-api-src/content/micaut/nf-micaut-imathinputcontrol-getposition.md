---
UID: NF:micaut.IMathInputControl.GetPosition
title: IMathInputControl::GetPosition
author: windows-sdk-content
description: Retrieves the position and size of the control.
old-location: tablet\imathinputcontrol_getposition.htm
old-project: tablet
ms.assetid: 4928f92d-7150-434c-abe4-d65a48ce1a56
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetPosition, GetPosition method [Tablet PC], GetPosition method [Tablet PC],IMathInputControl interface, IMathInputControl interface [Tablet PC],GetPosition method, IMathInputControl.GetPosition, IMathInputControl::GetPosition, micaut/IMathInputControl::GetPosition, tablet.imathinputcontrol_getposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.redist: 
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
 - IMathInputControl.GetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::GetPosition


## -description


Retrieves the position and size of the control.


## -parameters




### -param Left [out]

The leftmost position of the control.


### -param Top [out]

The highest position of the control.


### -param Right [out]

The rightmost position of the control.


### -param Bottom [out]

The lowest position of the control.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the control size and position even if the control is not visible.

This method returns the minimal possible width and height of the control if it is  called immediatelly after creation of the control.




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>



<a href="https://msdn.microsoft.com/9b5fc988-7c93-47d4-8661-4cef56cab0d0">SetPosition</a>
 

 

