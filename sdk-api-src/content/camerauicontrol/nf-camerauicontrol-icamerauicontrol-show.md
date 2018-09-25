---
UID: NF:camerauicontrol.ICameraUIControl.Show
title: ICameraUIControl::Show
author: windows-sdk-content
description: Displays the user interface control for the camera.
old-location: winprog\icamerauicontrol_show.htm
tech.root: devnotes
ms.assetid: 0426a6ce-9d3e-4ce1-8be8-5d216edc9f2f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ICameraUIControl interface [Windows API],Show method, ICameraUIControl.Show, ICameraUIControl::Show, Show, Show method [Windows API], Show method [Windows API],ICameraUIControl interface, camerauicontrol/ICameraUIControl::Show, winprog.icamerauicontrol_show
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: camerauicontrol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CameraUIControl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - camerauicontrol.h
api_name:
 - ICameraUIControl.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraUIControl::Show


## -description


Displays the user interface control for the camera.


## -parameters




### -param pWindow [in]

Pointer to the user interface window.


### -param mode [in]

Specifies whether the user interface will be presented in a browseable or linear manner.


### -param selectionMode

TBD


### -param captureMode [in]

Specifies whether the user interface that will be shown allows the user to capture a photo, capture a video, or either.


### -param photoFormat [in]

Provides the format for capturing photos. The available formats include JPEG, PNG, and JPEG XR.


### -param videoFormat [in]

Provides the format for capturing videos. The available formats include MP4 and WMV.


### -param bHasCloseButton [in]

TRUE if the user interface has a close button, otherwise, FALSE.


### -param pEventCallback [in]

Pointer to an event callback for the dialog. The callback is invoked if an item is captured or deleted, and when the dialog starts, or is closed or suspended.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh802717(v=VS.85).aspx">ICameraUIControl</a>
 

 

