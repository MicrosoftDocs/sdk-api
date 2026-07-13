---
UID: NF:imapi2.IDiscRecorder2Ex.GetByteAlignmentMask
title: IDiscRecorder2Ex::GetByteAlignmentMask (imapi2.h)
description: Retrieves the byte alignment mask for the device.
helpviewer_keywords: ["GetByteAlignmentMask","GetByteAlignmentMask method [IMAPI]","GetByteAlignmentMask method [IMAPI]","IDiscRecorder2Ex interface","IDiscRecorder2Ex interface [IMAPI]","GetByteAlignmentMask method","IDiscRecorder2Ex.GetByteAlignmentMask","IDiscRecorder2Ex::GetByteAlignmentMask","imapi.idiscrecorder2ex_getbytealignmentmask","imapi2/IDiscRecorder2Ex::GetByteAlignmentMask"]
old-location: imapi\idiscrecorder2ex_getbytealignmentmask.htm
tech.root: imapi
ms.assetid: 6a92efb1-4da8-4cf4-8011-b06a0f82a3eb
ms.date: 12/05/2018
ms.keywords: GetByteAlignmentMask, GetByteAlignmentMask method [IMAPI], GetByteAlignmentMask method [IMAPI],IDiscRecorder2Ex interface, IDiscRecorder2Ex interface [IMAPI],GetByteAlignmentMask method, IDiscRecorder2Ex.GetByteAlignmentMask, IDiscRecorder2Ex::GetByteAlignmentMask, imapi.idiscrecorder2ex_getbytealignmentmask, imapi2/IDiscRecorder2Ex::GetByteAlignmentMask
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
 - IDiscRecorder2Ex::GetByteAlignmentMask
 - imapi2/IDiscRecorder2Ex::GetByteAlignmentMask
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
 - IDiscRecorder2Ex.GetByteAlignmentMask
---

# IDiscRecorder2Ex::GetByteAlignmentMask


## -description

Retrieves the byte alignment mask for the device.

## -parameters

### -param value [out]

Byte alignment mask that you use to determine if the buffer is aligned to the correct byte boundary for the device. The byte alignment value is always a number that is a power of 2.

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

The data buffer for <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandsenddatatodevice">IDiscRecorder2Ex::SendCommandSendDataToDevice</a> and <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandgetdatafromdevice">IDiscRecorder2Ex::SendCommandGetDataFromDevice</a> must aligned to the correct byte boundary. To determine if the buffer is on the correct byte boundary, perform a bitwise logical AND of the bitmask with  the address of the data buffer. For example, if the address of the buffer is 0x3840958, you can test for correct alignment using the following statement:


``` syntax
if (0x3840958 & (value - 1) == 0)
{
    // The alignment is correct
}
```


## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandgetdatafromdevice">IDiscRecorder2Ex::SendCommandGetDataFromDevice</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandnodata">IDiscRecorder2Ex::SendCommandNoData</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandsenddatatodevice">IDiscRecorder2Ex::SendCommandSendDataToDevice</a>
