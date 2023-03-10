---
UID: NF:mfidl.IMFSensorProfileCollection.FindProfile
title: IMFSensorProfileCollection::FindProfile (mfidl.h)
description: Finds a profile based on the specified profile ID.
helpviewer_keywords: ["FindProfile","FindProfile method [Media Foundation]","FindProfile method [Media Foundation]","IMFSensorProfileCollection interface","IMFSensorProfileCollection interface [Media Foundation]","FindProfile method","IMFSensorProfileCollection.FindProfile","IMFSensorProfileCollection::FindProfile","mf.imfsensorprofilecollection_findprofile","mfidl/IMFSensorProfileCollection::FindProfile"]
old-location: mf\imfsensorprofilecollection_findprofile.htm
tech.root: mf
ms.assetid: 3EC77F69-717F-404F-9C8C-F420F360CB83
ms.date: 12/05/2018
ms.keywords: FindProfile, FindProfile method [Media Foundation], FindProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],FindProfile method, IMFSensorProfileCollection.FindProfile, IMFSensorProfileCollection::FindProfile, mf.imfsensorprofilecollection_findprofile, mfidl/IMFSensorProfileCollection::FindProfile
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorProfileCollection::FindProfile
 - mfidl/IMFSensorProfileCollection::FindProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.lib
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfileCollection.FindProfile
---

# IMFSensorProfileCollection::FindProfile


## -description

Finds a profile based on the specified profile ID.

## -parameters

### -param ProfileId [in]

Pointer to the The ID of the profile to find.

### -param ppProfile [out]

On success, returns a double pointer to the profile.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection">IMFSensorProfileCollection</a>