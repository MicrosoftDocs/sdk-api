---
UID: NS:mfidl._MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
title: MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA (mfidl.h)
description: Advises the secure processor of the Multimedia Class Scheduler service (MMCSS) parameters so that real-time tasks can be scheduled at the expected priority.
helpviewer_keywords: ["MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA","MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA structure [Media Foundation]","mf.mfcontentprotectiondevice_realtimeclient_data","mfidl/MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA"]
old-location: mf\mfcontentprotectiondevice_realtimeclient_data.htm
tech.root: mf
ms.assetid: E0A98B31-13D4-4281-AFFB-A3DA664CE876
ms.date: 12/05/2018
ms.keywords: MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA, MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA structure [Media Foundation], mf.mfcontentprotectiondevice_realtimeclient_data, mfidl/MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
 - mfidl/_MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
 - MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
 - mfidl/MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
---

# MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA structure


## -description

Advises the secure processor of the  Multimedia Class Scheduler service (MMCSS) parameters so that real-time tasks can be scheduled at the expected priority.

## -struct-fields

### -field TaskIndex

The identifier for the MMCSS task.

### -field ClassName

The name of the MMCSS task.

### -field BasePriority

The base priority of the thread that runs the MMCSS task.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>