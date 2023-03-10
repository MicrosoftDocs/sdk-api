---
UID: NF:camerauicontrol.ICameraUIControl.GetCurrentViewType
title: ICameraUIControl::GetCurrentViewType (camerauicontrol.h)
description: Gets the type of the current view.
helpviewer_keywords: ["GetCurrentViewType","GetCurrentViewType method [Windows API]","GetCurrentViewType method [Windows API]","ICameraUIControl interface","ICameraUIControl interface [Windows API]","GetCurrentViewType method","ICameraUIControl.GetCurrentViewType","ICameraUIControl::GetCurrentViewType","camerauicontrol/ICameraUIControl::GetCurrentViewType","winprog.icamerauicontrol_getcurrentviewtype"]
old-location: winprog\icamerauicontrol_getcurrentviewtype.htm
tech.root: winprog
ms.assetid: 1037db43-58db-4131-9a7d-d392250e133a
ms.date: 12/05/2018
ms.keywords: GetCurrentViewType, GetCurrentViewType method [Windows API], GetCurrentViewType method [Windows API],ICameraUIControl interface, ICameraUIControl interface [Windows API],GetCurrentViewType method, ICameraUIControl.GetCurrentViewType, ICameraUIControl::GetCurrentViewType, camerauicontrol/ICameraUIControl::GetCurrentViewType, winprog.icamerauicontrol_getcurrentviewtype
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICameraUIControl::GetCurrentViewType
 - camerauicontrol/ICameraUIControl::GetCurrentViewType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - camerauicontrol.h
api_name:
 - ICameraUIControl.GetCurrentViewType
---

# ICameraUIControl::GetCurrentViewType


## -description

Gets the type of the current view.

## -parameters

### -param pViewType [out]

A value that indicates whether the UI presents single items or lists of items.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/camerauicontrol/nn-camerauicontrol-icamerauicontrol">ICameraUIControl</a>