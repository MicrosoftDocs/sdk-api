---
UID: NF:mfidl.MFCreateTrackedSample
title: MFCreateTrackedSample function (mfidl.h)
description: Creates an IMFTrackedSample object that tracks the reference counts on a video media sample.
helpviewer_keywords: ["MFCreateTrackedSample","MFCreateTrackedSample function [Media Foundation]","mf.mfcreatetrackedsample","mfidl/MFCreateTrackedSample"]
old-location: mf\mfcreatetrackedsample.htm
tech.root: mf
ms.assetid: 05FB8F94-94B2-46A5-A890-E37E501233E2
ms.date: 12/05/2018
ms.keywords: MFCreateTrackedSample, MFCreateTrackedSample function [Media Foundation], mf.mfcreatetrackedsample, mfidl/MFCreateTrackedSample
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFCreateTrackedSample
 - mfidl/MFCreateTrackedSample
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
 - MFCreateTrackedSample
---

# MFCreateTrackedSample function


## -description

Creates an <a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample">IMFTrackedSample</a> object that tracks the reference counts on a video media sample.

## -parameters

### -param ppMFSample [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample">IMFTrackedSample</a> interface.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>