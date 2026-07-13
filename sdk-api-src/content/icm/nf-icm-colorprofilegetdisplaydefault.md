---
UID: NF:icm.ColorProfileGetDisplayDefault
tech.root: wcs
title: ColorProfileGetDisplayDefault
ms.date: 08/03/2022

targetos: Windows
description: ColorProfileGetDisplayDefault gets the default color profile for a given display in the specified scope.
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
 - ColorProfileGetDisplayDefault
f1_keywords:
 - ColorProfileGetDisplayDefault
 - icm/ColorProfileGetDisplayDefault
dev_langs:
 - c++
---

## -description

Gets the default color profile for a given display in the specified scope.

## -parameters

### -param scope

Specifies the association as system-wide or the current user.

### -param targetAdapterID

An identifier assigned to the adapter (e.g. GPU) of the target display. See [Remarks](#remarks) for more details.

### -param sourceID

An identifier assigned to the source of the display. See [Remarks](#remarks) for more details.

### -param profileType

The type of color profile to return (currently only CPT_ICC is supported).

### -param profileSubType

The subtype of the color profile to return.

### -param profileName

Receives a pointer to the default color profile name, which must be freed with [LocalFree](../winbase/nf-winbase-localfree.md).

## -returns

## -remarks

See [connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays) for information on display adapter IDs and source IDs.

## -see-also

[Connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays)
