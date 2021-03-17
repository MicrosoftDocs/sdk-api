---
UID: NF:mfidl.IMFSensorGroup.CreateMediaSource
title: IMFSensorGroup::CreateMediaSource (mfidl.h)
description: Creates an IMFMediaSource that virtualizes the sensor group.
helpviewer_keywords: ["CreateMediaSource","CreateMediaSource method [Media Foundation]","CreateMediaSource method [Media Foundation]","IMFSensorGroup interface","IMFSensorGroup interface [Media Foundation]","CreateMediaSource method","IMFSensorGroup.CreateMediaSource","IMFSensorGroup::CreateMediaSource","mf.imfsensorgroup_createmediasource","mfidl/IMFSensorGroup::CreateMediaSource"]
old-location: mf\imfsensorgroup_createmediasource.htm
tech.root: mf
ms.assetid: 2C69A81E-7159-43AA-92EA-7B1EB4A7A681
ms.date: 12/05/2018
ms.keywords: CreateMediaSource, CreateMediaSource method [Media Foundation], CreateMediaSource method [Media Foundation],IMFSensorGroup interface, IMFSensorGroup interface [Media Foundation],CreateMediaSource method, IMFSensorGroup.CreateMediaSource, IMFSensorGroup::CreateMediaSource, mf.imfsensorgroup_createmediasource, mfidl/IMFSensorGroup::CreateMediaSource
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorGroup::CreateMediaSource
 - mfidl/IMFSensorGroup::CreateMediaSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorGroup.CreateMediaSource
---

# IMFSensorGroup::CreateMediaSource


## -description

Creates an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> that virtualizes the sensor group. The term "device" in this context could refer to a physical device or a software media source. The source can represent a sensor group that actually contains multiple sensor devices, or it could contain only a single device, but still behaves as a sensor group.

## -parameters

### -param ppSource [out]

Receives a pointer to the created media source.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup">IMFSensorGroup</a>