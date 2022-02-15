---
UID: NF:camerauicontrol.ICameraUIControl.GetActiveItem
title: ICameraUIControl::GetActiveItem (camerauicontrol.h)
description: Gets the active captured item.
helpviewer_keywords: ["GetActiveItem","GetActiveItem method [Windows API]","GetActiveItem method [Windows API]","ICameraUIControl interface","ICameraUIControl interface [Windows API]","GetActiveItem method","ICameraUIControl.GetActiveItem","ICameraUIControl::GetActiveItem","camerauicontrol/ICameraUIControl::GetActiveItem","winprog.icamerauicontrol_getactiveitem"]
old-location: winprog\icamerauicontrol_getactiveitem.htm
tech.root: winprog
ms.assetid: 9ef05929-7292-4833-95e7-d420abb6cd43
ms.date: 12/05/2018
ms.keywords: GetActiveItem, GetActiveItem method [Windows API], GetActiveItem method [Windows API],ICameraUIControl interface, ICameraUIControl interface [Windows API],GetActiveItem method, ICameraUIControl.GetActiveItem, ICameraUIControl::GetActiveItem, camerauicontrol/ICameraUIControl::GetActiveItem, winprog.icamerauicontrol_getactiveitem
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
 - ICameraUIControl::GetActiveItem
 - camerauicontrol/ICameraUIControl::GetActiveItem
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
 - ICameraUIControl.GetActiveItem
---

# ICameraUIControl::GetActiveItem


## -description

Gets the active captured item.

## -parameters

### -param pbstrActiveItemPath [out]

Path to the currently active captured item.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/camerauicontrol/nn-camerauicontrol-icamerauicontrol">ICameraUIControl</a>