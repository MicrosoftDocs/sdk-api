---
UID: NE:deliveryoptimization._DODownloadState
tech.root: delivery_optimization
title: DODownloadState
ms.date: 05/04/2022
targetos: Windows
description: Specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.
req.construct-type: enumeration
req.ddi-compliance: 
req.header: deliveryoptimization.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DODownloadState
 - DODownloadState
f1_keywords:
 - _DODownloadState
 - deliveryoptimization/_DODownloadState
 - DODownloadState
 - deliveryoptimization/DODownloadState
dev_langs:
 - c++
helpviewer_keywords:
 - _DODownloadState
prerelease: false
---

## -description

The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.

## -enum-fields

### -field DODownloadState_Created

Download object is created but hasn't been started yet.

### -field DODownloadState_Transferring

Download is in progress.

### -field DODownloadState_Transferred

Download is transferred and can start again by downloading another portion of the file.

### -field DODownloadState_Finalized

Download is finalized and cannot be started again.

### -field DODownloadState_Aborted

Download was aborted.

### -field DODownloadState_Paused

Download has been paused on demand or due to transient error.

## -remarks

## -see-also
