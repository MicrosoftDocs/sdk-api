---
UID: NF:wtsapi32.WTSCloudAuthClose
tech.root: TermServ
title: WTSCloudAuthClose
ms.date: 09/25/2025
targetos: Windows
description: Closes a cloud authentication handle obtained by calling WTSCloudAuthOpen.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtsapi32.dll
api_name:
 - WTSCloudAuthClose
f1_keywords:
 - WTSCloudAuthClose
 - wtsapi32/WTSCloudAuthClose
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthClose
---

## -description

Closes a cloud authentication handle obtained by calling *[WTSCloudAuthOpen](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtscloudauthopen/)*.

## -parameters

### -param cloudAuthHandle [in]

The cloud authentication handle to close.

## -remarks

This function should be called to free resources associated with a cloud authentication handle when it is no longer needed.

## -see-also

