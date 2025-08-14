---
UID: NF:isolatedapplauncher.IsProcessInWDAGContainer
tech.root: winprog
title: IsProcessInWDAGContainer (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Determines if a process is running in a Microsoft Defender Application Guard (MDAG) container.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: isolatedapplauncher.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
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
 - api-ms-win-security-isolatedcontainer-l1-1-1.dll
 - isolatedapplauncher.h
api_name:
 - IsProcessInWDAGContainer
f1_keywords:
 - IsProcessInWDAGContainer
 - isolatedapplauncher/IsProcessInWDAGContainer
dev_langs:
 - c++
helpviewer_keywords:
 - IsProcessInWDAGContainer
---

## -description

Determines if a process is running in a Microsoft Defender Application Guard (MDAG) container.

## -parameters

### -param Reserved

This parameter is reserved for future use.

### -param isProcessInWDAGContainer

This indicates whether the process is running in a MDAG container.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

> [!NOTE]
> Windows Defender Application Guard (WDAG) is now Microsoft Defender Application Guard (MDAG). The WDAG name is deprecated, but it is still used in some APIs.

## -see-also
