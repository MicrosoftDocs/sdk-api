---
UID: NF:icm.ColorProfileGetDisplayList
tech.root: wcs
title: ColorProfileGetDisplayList
ms.date: 08/03/2022

targetos: Windows
description: ColorProfileGetDisplayList retrieves the list of profiles associated with a given display in the specified scope.
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
 - ColorProfileGetDisplayList
f1_keywords:
 - ColorProfileGetDisplayList
 - icm/ColorProfileGetDisplayList
dev_langs:
 - c++
---

## -description

Retrieves the list of profiles associated with a given display in the specified scope.

## -parameters

### -param scope

Specifies the association as system-wide or the current user.

### -param targetAdapterID

An identifier assigned to the adapter (e.g. GPU) of the target display. See [Remarks](#remarks) for more details.

### -param sourceID

An identifier assigned to the source of the display. See [Remarks](#remarks) for more details.

### -param profileList

Pointer to a buffer where the profile names are placed, must be freed with [LocalFree](../winbase/nf-winbase-localfree.md).

### -param profileCount

Receives the number of profiles names copied into profileList.

## -returns

**S_OK** for success, or a failure **HRESULT** value

## -remarks

See [connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays) for information on display adapter IDs and source IDs.

## -see-also

[Connecting and configuring displays](/windows-hardware/drivers/display/connecting-and-configuring-displays)
