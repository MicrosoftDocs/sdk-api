---
UID: NF:mfidl.IMFSensorProfileCollection.RemoveProfile
title: IMFSensorProfileCollection::RemoveProfile (mfidl.h)
description: Removes the specified profile based on the specified profile ID.
helpviewer_keywords: ["IMFSensorProfileCollection interface [Media Foundation]","RemoveProfile method","IMFSensorProfileCollection.RemoveProfile","IMFSensorProfileCollection::RemoveProfile","RemoveProfile","RemoveProfile method [Media Foundation]","RemoveProfile method [Media Foundation]","IMFSensorProfileCollection interface","mf.imfsensorprofilecollection_removeprofile","mfidl/IMFSensorProfileCollection::RemoveProfile"]
old-location: mf\imfsensorprofilecollection_removeprofile.htm
tech.root: mf
ms.assetid: E0A0C773-7B60-46C7-9B89-07DF5CAA1E84
ms.date: 12/05/2018
ms.keywords: IMFSensorProfileCollection interface [Media Foundation],RemoveProfile method, IMFSensorProfileCollection.RemoveProfile, IMFSensorProfileCollection::RemoveProfile, RemoveProfile, RemoveProfile method [Media Foundation], RemoveProfile method [Media Foundation],IMFSensorProfileCollection interface, mf.imfsensorprofilecollection_removeprofile, mfidl/IMFSensorProfileCollection::RemoveProfile
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
 - IMFSensorProfileCollection::RemoveProfile
 - mfidl/IMFSensorProfileCollection::RemoveProfile
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
 - IMFSensorProfileCollection.RemoveProfile
---

# IMFSensorProfileCollection::RemoveProfile


## -description

removes the specified profile based on the specified profile ID.

## -parameters

### -param ProfileId [in]

Pointer to the <a href="/windows/win32/api/mfidl/ns-mfidl-sensorprofileid">SENSORPROFILEID</a> of the profile to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection">IMFSensorProfileCollection</a>