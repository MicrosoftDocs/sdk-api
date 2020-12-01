---
UID: NF:mfidl.MFCreateSensorProfile
title: MFCreateSensorProfile function (mfidl.h)
description: Creates a sensor profile, based on the specified type, index, and optional constraints.
helpviewer_keywords: ["MFCreateSensorProfile","MFCreateSensorProfile function [Media Foundation]","mf.mfcreatesensorprofile","mfidl/MFCreateSensorProfile"]
old-location: mf\mfcreatesensorprofile.htm
tech.root: mf
ms.assetid: 76D14E98-0DB5-4D2C-9F6A-17D9B3CAA73E
ms.date: 12/05/2018
ms.keywords: MFCreateSensorProfile, MFCreateSensorProfile function [Media Foundation], mf.mfcreatesensorprofile, mfidl/MFCreateSensorProfile
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSensorProfile
 - mfidl/MFCreateSensorProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mfsensorgroup.dll
api_name:
 - MFCreateSensorProfile
---

# MFCreateSensorProfile function


## -description

Creates a sensor profile, based on the specified type, index, and optional constraints.

## -parameters

### -param ProfileType [in]

The profile type to create.

### -param ProfileIndex [in, out]

The profile index.

### -param Constraints [in, optional]

Any optional constraints to be put on the profile.

### -param ppProfile [out]

On success, returns a double pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a> containing the sensor profile.

## -returns

This function does not return a value.