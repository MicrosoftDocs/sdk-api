---
UID: NF:shdeprecated.IBrowserService.IsControlWindowShown
title: IBrowserService::IsControlWindowShown (shdeprecated.h)
description: Deprecated. Retrieves a value that indicates whether a specified frame control is currently visible.
helpviewer_keywords: ["FCW_INTERNETBAR","FCW_PROGRESS","FCW_STATUS","FCW_TOOLBAR","FCW_TREE","IBrowserService interface [Windows Shell]","IsControlWindowShown method","IBrowserService.IsControlWindowShown","IBrowserService::IsControlWindowShown","IsControlWindowShown","IsControlWindowShown method [Windows Shell]","IsControlWindowShown method [Windows Shell]","IBrowserService interface","shdeprecated/IBrowserService::IsControlWindowShown","shell.IBrowserService_IsControlWindowShown","zone_IBrowserService_IsControlWindowShown"]
old-location: shell\IBrowserService_IsControlWindowShown.htm
tech.root: shell
ms.assetid: fbbb83ce-be7c-4763-b2c4-2a05a460cbd6
ms.date: 12/05/2018
ms.keywords: FCW_INTERNETBAR, FCW_PROGRESS, FCW_STATUS, FCW_TOOLBAR, FCW_TREE, IBrowserService interface [Windows Shell],IsControlWindowShown method, IBrowserService.IsControlWindowShown, IBrowserService::IsControlWindowShown, IsControlWindowShown, IsControlWindowShown method [Windows Shell], IsControlWindowShown method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::IsControlWindowShown, shell.IBrowserService_IsControlWindowShown, zone_IBrowserService_IsControlWindowShown
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
 - IBrowserService::IsControlWindowShown
 - shdeprecated/IBrowserService::IsControlWindowShown
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
 - IBrowserService.IsControlWindowShown
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

