---
UID: NF:deliveryoptimization.IDODownloadStatusCallback.OnStatusChange
tech.root: delivery_optimization
title: IDODownloadStatusCallback::OnStatusChange
ms.date: 05/04/2022
targetos: Windows
description: Delivery Optimization calls your implementation of this method any time a download status has changed.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: deliveryoptimization.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - deliveryoptimization.h
api_name:
 - IDODownloadStatusCallback::OnStatusChange
f1_keywords:
 - IDODownloadStatusCallback::OnStatusChange
 - deliveryoptimization/IDODownloadStatusCallback::OnStatusChange
dev_langs:
 - c++
helpviewer_keywords:
 - OnStatusChange
prerelease: false
---

## -description

Delivery Optimization calls your implementation of this method any time a download status has changed.

## -parameters

### -param download

An pointer to the **IDODownload** interface whose status changed.

### -param status

A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
