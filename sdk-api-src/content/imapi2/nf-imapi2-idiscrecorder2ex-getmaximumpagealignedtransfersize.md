---
UID: NF:imapi2.IDiscRecorder2Ex.GetMaximumPageAlignedTransferSize
title: IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize (imapi2.h)
description: Retrieves the maximum page-aligned transfer size for the device.
helpviewer_keywords: ["GetMaximumPageAlignedTransferSize","GetMaximumPageAlignedTransferSize method [IMAPI]","GetMaximumPageAlignedTransferSize method [IMAPI]","IDiscRecorder2Ex interface","IDiscRecorder2Ex interface [IMAPI]","GetMaximumPageAlignedTransferSize method","IDiscRecorder2Ex.GetMaximumPageAlignedTransferSize","IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize","imapi.idiscrecorder2ex_getmaximumpagealignedtransfersize","imapi2/IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize"]
old-location: imapi\idiscrecorder2ex_getmaximumpagealignedtransfersize.htm
tech.root: imapi
ms.assetid: 6bf25c61-e87c-4ccf-a989-1c2715709d4a
ms.date: 12/05/2018
ms.keywords: GetMaximumPageAlignedTransferSize, GetMaximumPageAlignedTransferSize method [IMAPI], GetMaximumPageAlignedTransferSize method [IMAPI],IDiscRecorder2Ex interface, IDiscRecorder2Ex interface [IMAPI],GetMaximumPageAlignedTransferSize method, IDiscRecorder2Ex.GetMaximumPageAlignedTransferSize, IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize, imapi.idiscrecorder2ex_getmaximumpagealignedtransfersize, imapi2/IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize
 - imapi2/IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2Ex.GetMaximumPageAlignedTransferSize
---

# IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize


## -description

Retrieves the maximum page-aligned transfer size for the device.

## -parameters

### -param value [out]

Maximum size, in bytes,  of a page-aligned buffer.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>

## -remarks

Maximum page-aligned buffer size that a device can accept for a single command. The buffer for this transfer size must begin on a physical memory page boundary.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmaximumnonpagealignedtransfersize">IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize</a>