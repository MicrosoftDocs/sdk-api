---
UID: NF:imapi2.IDiscRecorder2Ex.GetMaximumNonPageAlignedTransferSize
title: IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize (imapi2.h)
description: Retrieves the maximum non-page-aligned transfer size for the device.
helpviewer_keywords: ["GetMaximumNonPageAlignedTransferSize","GetMaximumNonPageAlignedTransferSize method [IMAPI]","GetMaximumNonPageAlignedTransferSize method [IMAPI]","IDiscRecorder2Ex interface","IDiscRecorder2Ex interface [IMAPI]","GetMaximumNonPageAlignedTransferSize method","IDiscRecorder2Ex.GetMaximumNonPageAlignedTransferSize","IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize","imapi.idiscrecorder2ex_getmaximumnonpagealignedtransfersize","imapi2/IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize"]
old-location: imapi\idiscrecorder2ex_getmaximumnonpagealignedtransfersize.htm
tech.root: imapi
ms.assetid: dae56eb7-8fd5-40ea-b3de-2f98206a5cb2
ms.date: 12/05/2018
ms.keywords: GetMaximumNonPageAlignedTransferSize, GetMaximumNonPageAlignedTransferSize method [IMAPI], GetMaximumNonPageAlignedTransferSize method [IMAPI],IDiscRecorder2Ex interface, IDiscRecorder2Ex interface [IMAPI],GetMaximumNonPageAlignedTransferSize method, IDiscRecorder2Ex.GetMaximumNonPageAlignedTransferSize, IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize, imapi.idiscrecorder2ex_getmaximumnonpagealignedtransfersize, imapi2/IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize
f1_keywords:
- imapi2/IDiscRecorder2Ex.GetMaximumNonPageAlignedTransferSize
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- imapi2.h
api_name:
- IDiscRecorder2Ex.GetMaximumNonPageAlignedTransferSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscRecorder2Ex::GetMaximumNonPageAlignedTransferSize


## -description


Retrieves the maximum non-page-aligned transfer size for the device. 


## -parameters




### -param value [out]

Maximum size, in bytes,  of a non-page-aligned buffer.


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



This is the maximum buffer size that a device can accept for a single command. Buffers of this size provide the maximum exchange of data. The buffer does not need to begin on a  physical memory page boundary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-getmaximumpagealignedtransfersize">IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize</a>
 

 

