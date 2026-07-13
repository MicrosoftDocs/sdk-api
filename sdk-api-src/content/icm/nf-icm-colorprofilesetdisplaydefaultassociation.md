---
UID: NF:icm.ColorProfileSetDisplayDefaultAssociation
tech.root: wcs
title: ColorProfileSetDisplayDefaultAssociation
ms.date: 08/03/2022

targetos: Windows
description: ColorProfileSetDisplayDefaultAssociation sets an installed color profile as the default profile for a specified display in the given scope.
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
 - ColorProfileSetDisplayDefaultAssociation
f1_keywords:
 - ColorProfileSetDisplayDefaultAssociation
 - icm/ColorProfileSetDisplayDefaultAssociation
dev_langs:
 - c++
---

## -description

Sets an installed color profile as the default profile for a specified display in the given scope.

## -parameters

### -param scope

Specifies the association as system-wide or the current user.

### -param profileName

Identifies the installed profile to associate.

### -param profileType

The type of color profile to set as default (currently only CPT_ICC is supported).

### -param profileSubType

The subtype of the color profile to set as default.

### -param targetAdapterID

An identifier assigned to the adapter (e.g. GPU) of the target display. See [Remarks](#remarks) for more details.

### -param sourceID

An identifier assigned to the source of the display. See [Remarks](#remarks) for more details.

## -returns

**S_OK** for success, or a failure **HRESULT** value

## -remarks

See [connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays) for information on display adapter IDs and source IDs.

## -see-also

[Connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays)
