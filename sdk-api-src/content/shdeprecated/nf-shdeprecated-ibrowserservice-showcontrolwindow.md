---
UID: NF:shdeprecated.IBrowserService.ShowControlWindow
title: IBrowserService::ShowControlWindow (shdeprecated.h)
description: Deprecated. Shows or hides various frame controls.
helpviewer_keywords: ["FALSE","FCW_INTERNETBAR","FCW_PROGRESS","FCW_STATUS","FCW_TOOLBAR","FCW_TREE","IBrowserService interface [Windows Shell]","ShowControlWindow method","IBrowserService.ShowControlWindow","IBrowserService::ShowControlWindow","ShowControlWindow","ShowControlWindow method [Windows Shell]","ShowControlWindow method [Windows Shell]","IBrowserService interface","TRUE","shdeprecated/IBrowserService::ShowControlWindow","shell.IBrowserService_ShowControlWindow","zone_IBrowserService_ShowControlWindow"]
old-location: shell\IBrowserService_ShowControlWindow.htm
tech.root: shell
ms.assetid: 11ded544-6fba-41a5-bc61-222467fdbc05
ms.date: 12/05/2018
ms.keywords: FALSE, FCW_INTERNETBAR, FCW_PROGRESS, FCW_STATUS, FCW_TOOLBAR, FCW_TREE, IBrowserService interface [Windows Shell],ShowControlWindow method, IBrowserService.ShowControlWindow, IBrowserService::ShowControlWindow, ShowControlWindow, ShowControlWindow method [Windows Shell], ShowControlWindow method [Windows Shell],IBrowserService interface, TRUE, shdeprecated/IBrowserService::ShowControlWindow, shell.IBrowserService_ShowControlWindow, zone_IBrowserService_ShowControlWindow
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::ShowControlWindow
 - shdeprecated/IBrowserService::ShowControlWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.ShowControlWindow
---

# IBrowserService::ShowControlWindow


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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

