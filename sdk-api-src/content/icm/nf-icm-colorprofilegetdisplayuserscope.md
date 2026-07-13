---
UID: NF:icm.ColorProfileGetDisplayUserScope
tech.root: wcs
title: ColorProfileGetDisplayUserScope
ms.date: 08/03/2022

targetos: Windows
description: ColorProfileGetDisplayUserScope gets the currently selected color profile scope of the provided display - either user or system.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - icm.h
api_name:
 - ColorProfileGetDisplayUserScope
f1_keywords:
 - ColorProfileGetDisplayUserScope
 - icm/ColorProfileGetDisplayUserScope
dev_langs:
 - c++
---

## -description

Gets the currently selected color profile scope of the provided display - either user or system.

## -parameters

### -param targetAdapterID

An identifier assigned to the adapter (e.g. GPU) of the target display. See [Remarks](#remarks) for more details.

### -param sourceID

An identifier assigned to the source of the display. See [Remarks](#remarks) for more details.

### -param scope

Returns the scope of the currently selected color profile - either the current user or system.

## -returns

**S_OK** for success, or a failure **HRESULT** value

## -remarks

See [connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays) for information on display adapter IDs and source IDs.

## -see-also

[Connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays)
