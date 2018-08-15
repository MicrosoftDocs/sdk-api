---
UID: NF:npapi.NPDeviceMode
title: NPDeviceMode function
author: windows-sdk-content
description: Specifies the parent window of a device. This window owns any dialog boxes that originate from the device.
old-location: security\npdevicemode.htm
old-project: secauthn
ms.assetid: 502e3d34-f582-4f0f-b3b2-263bd293cf11
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NPDeviceMode, NPDeviceMode function [Security], _mnp_npdevicemode, npapi/NPDeviceMode, security.npdevicemode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: npapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NOTIFICATION_USER_INPUT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPDeviceMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NPDeviceMode function


## -description


The <b>NPDeviceMode</b> function specifies the parent window of a device. This window owns any dialog boxes that originate from the device.


## -parameters




### -param hParent [in]

A handle to the window that owns dialog boxes originating from this device.


## -returns



If the function succeeds, it will return WN_SUCCESS. Otherwise, it will return a Windows error code.



