---
UID: NF:deliveryoptimization.IDODownload.GetStatus
tech.root: delivery_optimization
title: IDODownload::GetStatus
ms.date: 08/03/2022
targetos: Windows
description: IDODownload::GetStatus retrieves a pointer to a DO_DOWNLOAD_STATUS structure that reflects the current status of the download.
req.assembly: Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.
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
 - IDODownload::GetStatus
f1_keywords:
 - IDODownload::GetStatus
 - deliveryoptimization/IDODownload::GetStatus
dev_langs:
 - c++
helpviewer_keywords:
 - GetStatus
prerelease: false
---

## -description

Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.

## -parameters

### -param status

A pointer to a **DO_DOWNLOAD_STATUS** structure.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
