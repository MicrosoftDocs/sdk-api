---
UID: NF:deliveryoptimization.IDODownload.Start
tech.root: delivery_optimization
title: IDODownload::Start
ms.date: 03/15/2023
targetos: Windows
description: Starts or resumes a download.
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
 - IDODownload::Start
f1_keywords:
 - IDODownload::Start
 - deliveryoptimization/IDODownload::Start
dev_langs:
 - c++
helpviewer_keywords:
 - Start
prerelease: false
---

## -description

Starts or resumes a download, passing optional ranges as a pointer to [DO_DOWNLOAD_RANGES_INFO](/windows/win32/api/deliveryoptimization/ns-deliveryoptimization-do_download_ranges_info) structure.


## -parameters

### -param ranges

Optional. A pointer to a [DO_DOWNLOAD_RANGES_INFO](/windows/win32/api/deliveryoptimization/ns-deliveryoptimization-do_download_ranges_info) structure (to download only specific ranges of the file). The value passed here indicates whether the download is for the entire file or partial ranges within the file or simply to resume the download without changing the ranges info. A request to download the entire file is indicated by passing a pointer to an empty DO_DOWNLOAD_RANGES_INFO structure, that is, with its RangeCount member set to zero. A request to download a partial file is indicated by passing a pointer to a non-empty DO_DOWNLOAD_RANGES_INFO structure. Passing `nullptr` is allowed only when download has already been started once before with empty/non-empty ranges, and indicates download must be resumed without any changes to the ranges requested.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
