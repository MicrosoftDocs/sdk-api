---
UID: NF:shdeprecated.IBrowserService.IsControlWindowShown
title: IBrowserService::IsControlWindowShown
author: windows-sdk-content
description: Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.
old-location: shell\IBrowserService_IsControlWindowShown.htm
tech.root: shell
ms.assetid: fbbb83ce-be7c-4763-b2c4-2a05a460cbd6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FCW_INTERNETBAR, FCW_PROGRESS, FCW_STATUS, FCW_TOOLBAR, FCW_TREE, IBrowserService interface [Windows Shell],IsControlWindowShown method, IBrowserService.IsControlWindowShown, IBrowserService::IsControlWindowShown, IsControlWindowShown, IsControlWindowShown method [Windows Shell], IsControlWindowShown method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::IsControlWindowShown, shell.IBrowserService_IsControlWindowShown, zone_IBrowserService_IsControlWindowShown
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.IsControlWindowShown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::IsControlWindowShown


## -description


Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.


## -parameters




### -param id [in]

Type: <b>UINT</b>

The frame control to check.

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


### -param pfShown [out]

Type: <b>BOOL*</b>

A value of type <b>BOOL</b> that indicates whether the specified frame control is visible.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



