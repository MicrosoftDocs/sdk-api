---
UID: NN:mfidl.IMFSensorGroup
title: IMFSensorGroup (mfidl.h)
description: Represents a group of sensor devices from which an IMFMediaSource can be created.
helpviewer_keywords: ["IMFSensorGroup","IMFSensorGroup interface [Media Foundation]","IMFSensorGroup interface [Media Foundation]","described","mf.imfsensorgroup","mfidl/IMFSensorGroup"]
old-location: mf\imfsensorgroup.htm
tech.root: mf
ms.assetid: 7CED3EF6-E844-4B3A-8181-CA44FC4675EC
ms.date: 12/05/2018
ms.keywords: IMFSensorGroup, IMFSensorGroup interface [Media Foundation], IMFSensorGroup interface [Media Foundation],described, mf.imfsensorgroup, mfidl/IMFSensorGroup
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
 - IMFSensorGroup
 - mfidl/IMFSensorGroup
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
 - IMFSensorGroup
---

# IMFSensorGroup interface


## -description

Represents a group of sensor devices from which an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> can be created. The term "device" in this context could refer to a physical device, a custom media source, or a frame provider. A sensor group may actually contain multiple sensor devices, or it could contain only a single device, but it still behaves as a sensor group.

## -inheritance

The <b>IMFSensorGroup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorGroup</b> also has these types of members:

