---
UID: NF:npapi.NPDeviceMode
title: NPDeviceMode function (npapi.h)
description: Specifies the parent window of a device. This window owns any dialog boxes that originate from the device.
helpviewer_keywords: ["NPDeviceMode","NPDeviceMode function [Security]","_mnp_npdevicemode","npapi/NPDeviceMode","security.npdevicemode"]
old-location: security\npdevicemode.htm
tech.root: security
ms.assetid: 502e3d34-f582-4f0f-b3b2-263bd293cf11
ms.date: 12/05/2018
ms.keywords: NPDeviceMode, NPDeviceMode function [Security], _mnp_npdevicemode, npapi/NPDeviceMode, security.npdevicemode
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPDeviceMode
 - npapi/NPDeviceMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPDeviceMode
---

# NPDeviceMode function


## -description

The <b>NPDeviceMode</b> function specifies the parent window of a device. This window owns any dialog boxes that originate from the device.

## -parameters

### -param hParent [in]

A handle to the window that owns dialog boxes originating from this device.

## -returns

If the function succeeds, it will return WN_SUCCESS. Otherwise, it will return a Windows error code.

