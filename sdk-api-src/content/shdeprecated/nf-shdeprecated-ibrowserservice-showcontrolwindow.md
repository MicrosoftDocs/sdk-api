---
UID: NF:shdeprecated.IBrowserService.ShowControlWindow
title: IBrowserService::ShowControlWindow method
author: windows-driver-content
description: Deprecated. Shows or hides various frame controls.
old-location: shell\IBrowserService_ShowControlWindow.htm
old-project: shell
ms.assetid: 11ded544-6fba-41a5-bc61-222467fdbc05
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: FALSE, FCW_INTERNETBAR, FCW_PROGRESS, FCW_STATUS, FCW_TOOLBAR, FCW_TREE, IBrowserService, IBrowserService interface [Windows Shell], ShowControlWindow method, IBrowserService::ShowControlWindow, ShowControlWindow method [Windows Shell], ShowControlWindow method [Windows Shell], IBrowserService interface, ShowControlWindow,IBrowserService.ShowControlWindow, TRUE, shdeprecated/IBrowserService::ShowControlWindow, shell.IBrowserService_ShowControlWindow, zone_IBrowserService_ShowControlWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService.ShowControlWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::ShowControlWindow method


## -description


Deprecated. Shows or hides various frame controls.


## -parameters




### -param id [in]

Type: <b>UINT</b>


                    A value that indicates the frame control to show or hide. One of the following values as defined in Shobjidl.h or -1 for fullscreen/kiosk mode.



<div class="alert"><b>Note</b>  These frame controls may not be supported in future versions of Windows.</div>
<div> </div>


#### FCW_STATUS (0x0001)

The browser's status bar.



#### FCW_TOOLBAR (0x0002)

The browser's toolbar.



#### FCW_TREE (0x0003)

The browser's tree view.



#### FCW_INTERNETBAR (0x0006)

The browser's Media Bar.



#### FCW_PROGRESS (0x0008)

The browser's progress bar.


### -param fShow [in]

Type: <b>BOOL</b>

A value that indicates whether to show or hide the frame control.



#### TRUE

Show the control.



#### FALSE

Hide the control.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



