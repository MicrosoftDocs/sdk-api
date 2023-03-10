---
UID: NF:mfidl.MFCreateContentProtectionDevice
title: MFCreateContentProtectionDevice function (mfidl.h)
description: Creates an IMFContentProtectionDevice interface for the specified media protection system.
helpviewer_keywords: ["MFCreateContentProtectionDevice","MFCreateContentProtectionDevice function [Media Foundation]","mf.mfcreatecontentprotectiondevice","mfidl/MFCreateContentProtectionDevice"]
old-location: mf\mfcreatecontentprotectiondevice.htm
tech.root: mf
ms.assetid: 6C301184-255B-4FE7-8DD6-962B236F90A6
ms.date: 12/05/2018
ms.keywords: MFCreateContentProtectionDevice, MFCreateContentProtectionDevice function [Media Foundation], mf.mfcreatecontentprotectiondevice, mfidl/MFCreateContentProtectionDevice
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
 - MFCreateContentProtectionDevice
 - mfidl/MFCreateContentProtectionDevice
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
 - MFCreateContentProtectionDevice
---

# MFCreateContentProtectionDevice function


## -description

Creates an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a> interface for the specified media protection system.

## -parameters

### -param ProtectionSystemId [in]

The identifier of the media protection system for which you want to create the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a> interface.

### -param ContentProtectionDevice [out]

Pointer to the created <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a> interface.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>