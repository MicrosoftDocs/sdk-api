---
UID: NE:mfidl._MFSHUTDOWN_STATUS
title: MFSHUTDOWN_STATUS (mfidl.h)
description: Describes the current status of a call to the IMFShutdown::Shutdown method.
helpviewer_keywords: ["MFSHUTDOWN_COMPLETED","MFSHUTDOWN_INITIATED","MFSHUTDOWN_STATUS","MFSHUTDOWN_STATUS enumeration [Media Foundation]","a2257260-3f2c-4c6b-88cc-b8927b899782","mf.mfshutdown_status","mfidl/MFSHUTDOWN_COMPLETED","mfidl/MFSHUTDOWN_INITIATED","mfidl/MFSHUTDOWN_STATUS"]
old-location: mf\mfshutdown_status.htm
tech.root: mf
ms.assetid: a2257260-3f2c-4c6b-88cc-b8927b899782
ms.date: 12/05/2018
ms.keywords: MFSHUTDOWN_COMPLETED, MFSHUTDOWN_INITIATED, MFSHUTDOWN_STATUS, MFSHUTDOWN_STATUS enumeration [Media Foundation], a2257260-3f2c-4c6b-88cc-b8927b899782, mf.mfshutdown_status, mfidl/MFSHUTDOWN_COMPLETED, mfidl/MFSHUTDOWN_INITIATED, mfidl/MFSHUTDOWN_STATUS
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFSHUTDOWN_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFSHUTDOWN_STATUS
 - mfidl/_MFSHUTDOWN_STATUS
 - MFSHUTDOWN_STATUS
 - mfidl/MFSHUTDOWN_STATUS
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
 - MFSHUTDOWN_STATUS
---

# MFSHUTDOWN_STATUS enumeration


## -description

Describes the current status of a call to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a> method.

## -enum-fields

### -field MFSHUTDOWN_INITIATED:0

The shutdown operation has started but is not yet complete.

### -field MFSHUTDOWN_COMPLETED

Shutdown is complete.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus">IMFShutdown::GetShutdownStatus</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
