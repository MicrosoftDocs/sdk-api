---
UID: NF:mfidl.IMFSensorProfile.GetProfileId
title: IMFSensorProfile::GetProfileId (mfidl.h)
description: Retrieves the sensor profile ID.
helpviewer_keywords: ["GetProfileId","GetProfileId method [Media Foundation]","GetProfileId method [Media Foundation]","IMFSensorProfile interface","IMFSensorProfile interface [Media Foundation]","GetProfileId method","IMFSensorProfile.GetProfileId","IMFSensorProfile::GetProfileId","mf.imfsensorprofile_getprofileid","mfidl/IMFSensorProfile::GetProfileId"]
old-location: mf\imfsensorprofile_getprofileid.htm
tech.root: mf
ms.assetid: EBBDCC39-8FF9-421B-867D-0AD950C2DDF5
ms.date: 12/05/2018
ms.keywords: GetProfileId, GetProfileId method [Media Foundation], GetProfileId method [Media Foundation],IMFSensorProfile interface, IMFSensorProfile interface [Media Foundation],GetProfileId method, IMFSensorProfile.GetProfileId, IMFSensorProfile::GetProfileId, mf.imfsensorprofile_getprofileid, mfidl/IMFSensorProfile::GetProfileId
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - IMFSensorProfile::GetProfileId
 - mfidl/IMFSensorProfile::GetProfileId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfile.GetProfileId
---

# IMFSensorProfile::GetProfileId


## -description

Retrieves the sensor profile ID.

## -parameters

### -param pId [out]

Pointer to a <a href="/windows/win32/api/mfidl/ns-mfidl-sensorprofileid">SENSORPROFILEID</a> containing the profile ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a>