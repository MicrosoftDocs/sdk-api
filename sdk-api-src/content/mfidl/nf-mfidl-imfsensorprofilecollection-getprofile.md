---
UID: NF:mfidl.IMFSensorProfileCollection.GetProfile
title: IMFSensorProfileCollection::GetProfile (mfidl.h)
description: Retrieves the specified profile.
helpviewer_keywords: ["GetProfile","GetProfile method [Media Foundation]","GetProfile method [Media Foundation]","IMFSensorProfileCollection interface","IMFSensorProfileCollection interface [Media Foundation]","GetProfile method","IMFSensorProfileCollection.GetProfile","IMFSensorProfileCollection::GetProfile","mf.imfsensorprofilecollection_getprofile","mfidl/IMFSensorProfileCollection::GetProfile"]
old-location: mf\imfsensorprofilecollection_getprofile.htm
tech.root: mf
ms.assetid: 3E229A12-D53A-493F-9EFB-EA28131ABB10
ms.date: 12/05/2018
ms.keywords: GetProfile, GetProfile method [Media Foundation], GetProfile method [Media Foundation],IMFSensorProfileCollection interface, IMFSensorProfileCollection interface [Media Foundation],GetProfile method, IMFSensorProfileCollection.GetProfile, IMFSensorProfileCollection::GetProfile, mf.imfsensorprofilecollection_getprofile, mfidl/IMFSensorProfileCollection::GetProfile
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
 - IMFSensorProfileCollection::GetProfile
 - mfidl/IMFSensorProfileCollection::GetProfile
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
 - IMFSensorProfileCollection.GetProfile
---

# IMFSensorProfileCollection::GetProfile


## -description

Retrieves the specified profile.

## -parameters

### -param Index [in]

Index of the profile to retrieve.

### -param ppProfile [out]

On success, returns a double pointer to an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a> object that describes the specified sensor profile.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection">IMFSensorProfileCollection</a>