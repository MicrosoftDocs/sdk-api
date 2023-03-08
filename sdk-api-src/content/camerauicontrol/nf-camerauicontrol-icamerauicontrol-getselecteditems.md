---
UID: NF:camerauicontrol.ICameraUIControl.GetSelectedItems
title: ICameraUIControl::GetSelectedItems (camerauicontrol.h)
description: Gets the selected items.
helpviewer_keywords: ["GetSelectedItems","GetSelectedItems method [Windows API]","GetSelectedItems method [Windows API]","ICameraUIControl interface","ICameraUIControl interface [Windows API]","GetSelectedItems method","ICameraUIControl.GetSelectedItems","ICameraUIControl::GetSelectedItems","camerauicontrol/ICameraUIControl::GetSelectedItems","winprog.icamerauicontrol_getselecteditems"]
old-location: winprog\icamerauicontrol_getselecteditems.htm
tech.root: winprog
ms.assetid: 572cbf23-b9b5-441c-9bde-55ef856397ca
ms.date: 12/05/2018
ms.keywords: GetSelectedItems, GetSelectedItems method [Windows API], GetSelectedItems method [Windows API],ICameraUIControl interface, ICameraUIControl interface [Windows API],GetSelectedItems method, ICameraUIControl.GetSelectedItems, ICameraUIControl::GetSelectedItems, camerauicontrol/ICameraUIControl::GetSelectedItems, winprog.icamerauicontrol_getselecteditems
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
 - ICameraUIControl::GetSelectedItems
 - camerauicontrol/ICameraUIControl::GetSelectedItems
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
 - ICameraUIControl.GetSelectedItems
---

# ICameraUIControl::GetSelectedItems


## -description

Gets the selected items.

## -parameters

### -param ppSelectedItemPaths [out]

An array of paths to captured items selected in the user interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/camerauicontrol/nn-camerauicontrol-icamerauicontrol">ICameraUIControl</a>