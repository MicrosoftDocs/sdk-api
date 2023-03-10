---
UID: NS:ndkinfo.NDK_VERSION
title: NDK_VERSION (ndkinfo.h)
description: The NDK_VERSION structure specifies major and minor versions in the NDK interface.
helpviewer_keywords: ["NDK_VERSION","NDK_VERSION structure [Network Drivers Starting with Windows Vista]","ndkinfo/NDK_VERSION","netvista.ndk_version"]
old-location: netvista\ndk_version.htm
tech.root: NetVista
ms.assetid: 10A5A3E6-7257-4560-8452-607EC7C54397
ms.date: 12/05/2018
ms.keywords: NDK_VERSION, NDK_VERSION structure [Network Drivers Starting with Windows Vista], ndkinfo/NDK_VERSION, netvista.ndk_version
req.header: ndkinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NDK_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NDK_VERSION
 - ndkinfo/NDK_VERSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndkinfo.h
api_name:
 - NDK_VERSION
---

# NDK_VERSION structure


## -description

The <b>NDK_VERSION</b> structure specifies major and minor versions in the NDK interface.

## -struct-fields

### -field Major

The NDK major version number.

### -field Minor

The NDK minor version number.

## -remarks

This structure is used to specify NDK version numbers in several NDK structures and functions.

To specify version 1.1 (for Windows Server 2012), set both the <b>Major</b> and <b>Minor</b> members to 1.

To specify version 1.2 (for Windows Server 2012 R2), set the <b>Major</b> member to 1 and the <b>Minor</b> member to 2.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ndisndk/ns-ndisndk-_ndis_open_ndk_adapter_parameters">NDIS_OPEN_NDK_ADAPTER_PARAMETERS</a>



<a href="/windows/desktop/api/ndkinfo/ns-ndkinfo-ndk_adapter_info">NDK_ADAPTER_INFO</a>



<a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_query_extension_interface">NDK_FN_QUERY_EXTENSION_INTERFACE</a>



<a href="/windows-hardware/drivers/ddi/content/ndkpi/ns-ndkpi-_ndk_object_header">NDK_OBJECT_HEADER</a>

