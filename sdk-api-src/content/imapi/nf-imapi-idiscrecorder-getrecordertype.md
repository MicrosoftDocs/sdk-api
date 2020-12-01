---
UID: NF:imapi.IDiscRecorder.GetRecorderType
title: IDiscRecorder::GetRecorderType (imapi.h)
description: Determines whether the disc recorder is a CD-R or CD-RW type device. This does not indicate the type of media that is currently inserted in the device.
helpviewer_keywords: ["GetRecorderType","GetRecorderType method [IMAPI]","GetRecorderType method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetRecorderType method","IDiscRecorder.GetRecorderType","IDiscRecorder::GetRecorderType","RECORDER_CDR","RECORDER_CDRW","_win32_idiscrecorder_getrecordertype","base.idiscrecorder_getrecordertype","imapi.idiscrecorder_getrecordertype","imapi/IDiscRecorder::GetRecorderType"]
old-location: imapi\idiscrecorder_getrecordertype.htm
tech.root: imapi
ms.assetid: 287516b5-5d27-4277-8bc4-e2409b2a8cd7
ms.date: 12/05/2018
ms.keywords: GetRecorderType, GetRecorderType method [IMAPI], GetRecorderType method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderType method, IDiscRecorder.GetRecorderType, IDiscRecorder::GetRecorderType, RECORDER_CDR, RECORDER_CDRW, _win32_idiscrecorder_getrecordertype, base.idiscrecorder_getrecordertype, imapi.idiscrecorder_getrecordertype, imapi/IDiscRecorder::GetRecorderType
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder::GetRecorderType
 - imapi/IDiscRecorder::GetRecorderType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.GetRecorderType
---

# IDiscRecorder::GetRecorderType


## -description

Determines whether the disc recorder is a CD-R or CD-RW type device. This does not indicate the type of media that is currently inserted in the device.

## -parameters

### -param fTypeCode [out]

One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECORDER_CDR"></a><a id="recorder_cdr"></a><dl>
<dt><b>RECORDER_CDR</b></dt>
</dl>
</td>
<td width="60%">
0x1

</td>
</tr>
<tr>
<td width="40%"><a id="RECORDER_CDRW"></a><a id="recorder_cdrw"></a><dl>
<dt><b>RECORDER_CDRW</b></dt>
</dl>
</td>
<td width="60%">
0x2

</td>
</tr>
</table>

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>