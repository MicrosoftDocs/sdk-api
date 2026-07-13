---
UID: NF:deliveryoptimization.IDODownload.Finalize
tech.root: delivery_optimization
title: IDODownload::Finalize
ms.date: 05/04/2022
targetos: Windows
description: Finalizes the download.
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
 - IDODownload::Finalize
f1_keywords:
 - IDODownload::Finalize
 - deliveryoptimization/IDODownload::Finalize
dev_langs:
 - c++
helpviewer_keywords:
 - Finalize
prerelease: false
---

## -description

Finalizes the download. Once finalized, a download cannot be resumed by calling **Start**.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
