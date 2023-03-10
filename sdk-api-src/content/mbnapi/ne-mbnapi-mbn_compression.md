---
UID: NE:mbnapi.MBN_COMPRESSION
title: MBN_COMPRESSION (mbnapi.h)
description: The MBN_COMPRESSION enumerated type specifies whether compression is to be used in the data link for header and data.
helpviewer_keywords: ["MBN_COMPRESSION","MBN_COMPRESSION enumeration [Microsoft Broadband Networks]","MBN_COMPRESSION_ENABLE","MBN_COMPRESSION_NONE","mbn.mbn_compression","mbnapi/MBN_COMPRESSION","mbnapi/MBN_COMPRESSION_ENABLE","mbnapi/MBN_COMPRESSION_NONE"]
old-location: mbn\mbn_compression.htm
tech.root: mbn
ms.assetid: fd5cbfba-2eea-4d81-9733-33feb402fd8d
ms.date: 12/05/2018
ms.keywords: MBN_COMPRESSION, MBN_COMPRESSION enumeration [Microsoft Broadband Networks], MBN_COMPRESSION_ENABLE, MBN_COMPRESSION_NONE, mbn.mbn_compression, mbnapi/MBN_COMPRESSION, mbnapi/MBN_COMPRESSION_ENABLE, mbnapi/MBN_COMPRESSION_NONE
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
req.typenames: MBN_COMPRESSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_COMPRESSION
 - mbnapi/MBN_COMPRESSION
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
 - MBN_COMPRESSION
---

# MBN_COMPRESSION enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_COMPRESSION</b> enumerated type specifies whether compression is to be used in the data link for header and data.

This type is applicable only for GSM devices.

## -enum-fields

### -field MBN_COMPRESSION_NONE:0

Data headers are not compressed.

### -field MBN_COMPRESSION_ENABLE

Data headers are compressed.

