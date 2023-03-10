---
UID: NE:mbnapi.MBN_CONNECTION_MODE
title: MBN_CONNECTION_MODE (mbnapi.h)
description: The MBN_CONNECTION_MODE enumerated type specifies the mode of connection requested.
helpviewer_keywords: ["MBN_CONNECTION_MODE","MBN_CONNECTION_MODE enumeration [Microsoft Broadband Networks]","MBN_CONNECTION_MODE_PROFILE","MBN_CONNECTION_MODE_TMP_PROFILE","mbn.mbn_connection_mode","mbnapi/MBN_CONNECTION_MODE","mbnapi/MBN_CONNECTION_MODE_PROFILE","mbnapi/MBN_CONNECTION_MODE_TMP_PROFILE"]
old-location: mbn\mbn_connection_mode.htm
tech.root: mbn
ms.assetid: c7aed29b-7938-4266-ae4c-b8ba84eb8a63
ms.date: 12/05/2018
ms.keywords: MBN_CONNECTION_MODE, MBN_CONNECTION_MODE enumeration [Microsoft Broadband Networks], MBN_CONNECTION_MODE_PROFILE, MBN_CONNECTION_MODE_TMP_PROFILE, mbn.mbn_connection_mode, mbnapi/MBN_CONNECTION_MODE, mbnapi/MBN_CONNECTION_MODE_PROFILE, mbnapi/MBN_CONNECTION_MODE_TMP_PROFILE
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
req.typenames: MBN_CONNECTION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_CONNECTION_MODE
 - mbnapi/MBN_CONNECTION_MODE
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
 - MBN_CONNECTION_MODE
---

# MBN_CONNECTION_MODE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_CONNECTION_MODE</b> enumerated type specifies the mode of connection requested.

## -enum-fields

### -field MBN_CONNECTION_MODE_PROFILE:0

Profile name is used for connection.

### -field MBN_CONNECTION_MODE_TMP_PROFILE

A string representing the XML profile is used for connection.

