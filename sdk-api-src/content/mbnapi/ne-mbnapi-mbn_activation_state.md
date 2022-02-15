---
UID: NE:mbnapi.MBN_ACTIVATION_STATE
title: MBN_ACTIVATION_STATE (mbnapi.h)
description: The MBN_ACTIVATION_STATE enumerated type indicates the current data connection state.
helpviewer_keywords: ["MBN_ACTIVATION_STATE","MBN_ACTIVATION_STATE enumeration [Microsoft Broadband Networks]","MBN_ACTIVATION_STATE_ACTIVATED","MBN_ACTIVATION_STATE_ACTIVATING","MBN_ACTIVATION_STATE_DEACTIVATED","MBN_ACTIVATION_STATE_DEACTIVATING","MBN_ACTIVATION_STATE_NONE","mbn.mbn_activation_state","mbnapi/MBN_ACTIVATION_STATE","mbnapi/MBN_ACTIVATION_STATE_ACTIVATED","mbnapi/MBN_ACTIVATION_STATE_ACTIVATING","mbnapi/MBN_ACTIVATION_STATE_DEACTIVATED","mbnapi/MBN_ACTIVATION_STATE_DEACTIVATING","mbnapi/MBN_ACTIVATION_STATE_NONE"]
old-location: mbn\mbn_activation_state.htm
tech.root: mbn
ms.assetid: 712b9ead-8e38-45b1-8dff-b8906056d3d6
ms.date: 12/05/2018
ms.keywords: MBN_ACTIVATION_STATE, MBN_ACTIVATION_STATE enumeration [Microsoft Broadband Networks], MBN_ACTIVATION_STATE_ACTIVATED, MBN_ACTIVATION_STATE_ACTIVATING, MBN_ACTIVATION_STATE_DEACTIVATED, MBN_ACTIVATION_STATE_DEACTIVATING, MBN_ACTIVATION_STATE_NONE, mbn.mbn_activation_state, mbnapi/MBN_ACTIVATION_STATE, mbnapi/MBN_ACTIVATION_STATE_ACTIVATED, mbnapi/MBN_ACTIVATION_STATE_ACTIVATING, mbnapi/MBN_ACTIVATION_STATE_DEACTIVATED, mbnapi/MBN_ACTIVATION_STATE_DEACTIVATING, mbnapi/MBN_ACTIVATION_STATE_NONE
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MBN_ACTIVATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_ACTIVATION_STATE
 - mbnapi/MBN_ACTIVATION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_ACTIVATION_STATE
---

# MBN_ACTIVATION_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_ACTIVATION_STATE</b> enumerated type indicates the current data connection state.

## -enum-fields

### -field MBN_ACTIVATION_STATE_NONE:0

The connection state is unknown.

### -field MBN_ACTIVATION_STATE_ACTIVATED

The connection has been established.

### -field MBN_ACTIVATION_STATE_ACTIVATING

The device is establishing the connection.

### -field MBN_ACTIVATION_STATE_DEACTIVATED

There is no connection.

### -field MBN_ACTIVATION_STATE_DEACTIVATING

The device is in the process of disconnection.

