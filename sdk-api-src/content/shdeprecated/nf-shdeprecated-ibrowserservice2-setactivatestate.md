---
UID: NF:shdeprecated.IBrowserService2.SetActivateState
title: IBrowserService2::SetActivateState (shdeprecated.h)
description: Deprecated. Updates the value of the _uActivateState member of the BASEBROWSERDATA structure, which tracks whether the browser view window is in an activated state. The derived class makes this call to the base class.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","SetActivateState method","IBrowserService2.SetActivateState","IBrowserService2::SetActivateState","SetActivateState","SetActivateState method [Windows Shell]","SetActivateState method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::SetActivateState","shell.IBrowserService2_SetActivateState","zone_IBrowserService2_SetActivateState"]
old-location: shell\IBrowserService2_SetActivateState.htm
tech.root: shell
ms.assetid: 7a822b69-892d-48dc-99b3-8d725036722d
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],SetActivateState method, IBrowserService2.SetActivateState, IBrowserService2::SetActivateState, SetActivateState, SetActivateState method [Windows Shell], SetActivateState method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::SetActivateState, shell.IBrowserService2_SetActivateState, zone_IBrowserService2_SetActivateState
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::SetActivateState
 - shdeprecated/IBrowserService2::SetActivateState
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
 - IBrowserService2.SetActivateState
---

# IBrowserService2::SetActivateState


## -description

Deprecated. Updates the value of the <b>_uActivateState</b> member of the <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure, which tracks whether the browser view window is in an activated state. The derived class makes this call to the base class.

## -parameters

### -param u [in]

Type: <b>UINT</b>

The activation state of the window. This is always the SVUIA_ACTIVATE_FOCUS (0x0002) value from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status">SVUIA_STATUS</a> enumeration defined in Shobjidl.h.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.