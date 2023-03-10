---
UID: NF:mfidl.MFIsContentProtectionDeviceSupported
title: MFIsContentProtectionDeviceSupported function (mfidl.h)
description: Checks whether a hardware security processor is supported for the specified media protection system.
helpviewer_keywords: ["MFIsContentProtectionDeviceSupported","MFIsContentProtectionDeviceSupported function [Media Foundation]","mf.mfiscontentprotectiondevicesupported","mfidl/MFIsContentProtectionDeviceSupported"]
old-location: mf\mfiscontentprotectiondevicesupported.htm
tech.root: mf
ms.assetid: 8C91C204-49C0-41CF-A9E1-F9C53388604A
ms.date: 12/05/2018
ms.keywords: MFIsContentProtectionDeviceSupported, MFIsContentProtectionDeviceSupported function [Media Foundation], mf.mfiscontentprotectiondevicesupported, mfidl/MFIsContentProtectionDeviceSupported
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFIsContentProtectionDeviceSupported
 - mfidl/MFIsContentProtectionDeviceSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFIsContentProtectionDeviceSupported
---

# MFIsContentProtectionDeviceSupported function


## -description

Checks whether a hardware security processor is supported for the specified media protection system.

## -parameters

### -param ProtectionSystemId [in]

The identifier of the protection system that you want to check.

### -param isSupported [out]

<b>TRUE</b> if the hardware security processor is supported for the specified protection system; otherwise <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>