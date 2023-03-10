---
UID: NF:mfidl.IMFSensorProfile.AddProfileFilter
title: IMFSensorProfile::AddProfileFilter (mfidl.h)
description: Adds a profile filter to the specified media stream.
helpviewer_keywords: ["AddProfileFilter","AddProfileFilter method [Media Foundation]","AddProfileFilter method [Media Foundation]","IMFSensorProfile interface","IMFSensorProfile interface [Media Foundation]","AddProfileFilter method","IMFSensorProfile.AddProfileFilter","IMFSensorProfile::AddProfileFilter","mf.imfsensorprofile_addprofilefilter","mfidl/IMFSensorProfile::AddProfileFilter"]
old-location: mf\imfsensorprofile_addprofilefilter.htm
tech.root: mf
ms.assetid: D79C83AA-A105-4320-80D8-F7A3753DF4C4
ms.date: 12/05/2018
ms.keywords: AddProfileFilter, AddProfileFilter method [Media Foundation], AddProfileFilter method [Media Foundation],IMFSensorProfile interface, IMFSensorProfile interface [Media Foundation],AddProfileFilter method, IMFSensorProfile.AddProfileFilter, IMFSensorProfile::AddProfileFilter, mf.imfsensorprofile_addprofilefilter, mfidl/IMFSensorProfile::AddProfileFilter
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
 - IMFSensorProfile::AddProfileFilter
 - mfidl/IMFSensorProfile::AddProfileFilter
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
 - IMFSensorProfile.AddProfileFilter
---

# IMFSensorProfile::AddProfileFilter


## -description

Adds a profile filter to the specified media stream.

## -parameters

### -param StreamId [in]

The ID of the stream to add to.

### -param wzFilterSetString [in]

The filter to add.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a>