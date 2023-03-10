---
UID: NF:bits10_3.IBackgroundCopyJobHttpOptions3.MakeCustomHeadersWriteOnly
title: IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly
ms.keywords: IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly
description: Sets the HTTP custom headers for this job to be write-only.
helpviewer_keywords: ["IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly"]
tech.root: Bits
ms.date: 05/09/2019
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Bits.dll
req.header: bits10_3.h
req.idl: 
req.include-header: Bits.h
req.irql: 
req.kmdf-ver: 
req.lib: Bits.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly
 - bits10_3/IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - bits10_3.h
api_name:
 - IBackgroundCopyJobHttpOptions3::MakeCustomHeadersWriteOnly
---

## -description

Sets the HTTP custom headers for this job to be write-only. Write-only headers cannot be read by BITS methods such as the [IBackgroundCopyJobHttpOptions::GetCustomHeaders method](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-getcustomheaders).



## -returns

The return value is always **S_OK**.

## -remarks

Use this API when your BITS custom headers must include security information (such as an API token) that you don't want to be readable by other programs running on the same computer. The BITS process, of course, can still read these headers, and send them over the HTTP connection. Once the headers are set to write-only, that cannot be unset.

## -see-also

