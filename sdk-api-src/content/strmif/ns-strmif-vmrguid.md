---
UID: NS:strmif.tagVMRGUID
title: VMRGUID (strmif.h)
description: The VMRGUID structure is a member of the VMRMONITORINFO structure and is used to identify a monitor on the system (VMR-7 only).
helpviewer_keywords: ["VMRGUID","VMRGUID structure [DirectShow]","VMRGUIDStructure","dshow.vmrguid","strmif/VMRGUID"]
old-location: dshow\vmrguid.htm
tech.root: dshow
ms.assetid: e05d986a-c044-47c9-8430-7190ad29c7ec
ms.date: 12/05/2018
ms.keywords: VMRGUID, VMRGUID structure [DirectShow], VMRGUIDStructure, dshow.vmrguid, strmif/VMRGUID
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: VMRGUID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVMRGUID
 - strmif/tagVMRGUID
 - VMRGUID
 - strmif/VMRGUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRGUID
---

# VMRGUID structure


## -description

The [VMRMONITORINFO](/windows/desktop/api/strmif/ns-strmif-vmrmonitorinfo) structure and is used to identify a monitor on the system (VMR-7 only).

## -struct-fields

### -field pGUID

Pointer to the GUID member of the structure. <b>pGUID</b> is <b>NULL</b> if the monitor is the default DirectDraw device.

### -field GUID

Specifies the GUID for the monitor.

## -remarks

In DirectX 9.0 and later, the monitor is identified by an integer index, not by a GUID.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>