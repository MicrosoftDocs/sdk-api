---
UID: NF:imapi.IDiscRecorder.GetRecorderState
title: IDiscRecorder::GetRecorderState (imapi.h)
description: Retrieves the disc recorder state.
helpviewer_keywords: ["GetRecorderState","GetRecorderState method [IMAPI]","GetRecorderState method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetRecorderState method","IDiscRecorder.GetRecorderState","IDiscRecorder::GetRecorderState","RECORDER_BURNING","RECORDER_DOING_NOTHING","RECORDER_OPENED","_win32_idiscrecorder_getrecorderstate","base.idiscrecorder_getrecorderstate","imapi.idiscrecorder_getrecorderstate","imapi/IDiscRecorder::GetRecorderState"]
old-location: imapi\idiscrecorder_getrecorderstate.htm
tech.root: imapi
ms.assetid: 7fa57f8b-33c4-475c-958c-1e2c4973e23a
ms.date: 12/05/2018
ms.keywords: GetRecorderState, GetRecorderState method [IMAPI], GetRecorderState method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetRecorderState method, IDiscRecorder.GetRecorderState, IDiscRecorder::GetRecorderState, RECORDER_BURNING, RECORDER_DOING_NOTHING, RECORDER_OPENED, _win32_idiscrecorder_getrecorderstate, base.idiscrecorder_getrecorderstate, imapi.idiscrecorder_getrecorderstate, imapi/IDiscRecorder::GetRecorderState
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
 - IDiscRecorder::GetRecorderState
 - imapi/IDiscRecorder::GetRecorderState
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
 - IDiscRecorder.GetRecorderState
---

# IDiscRecorder::GetRecorderState


## -description

Retrieves the disc recorder state.

## -parameters

### -param pulDevStateFlags [out]

One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECORDER_BURNING"></a><a id="recorder_burning"></a><dl>
<dt><b>RECORDER_BURNING</b></dt>
</dl>
</td>
<td width="60%">
0x2

</td>
</tr>
<tr>
<td width="40%"><a id="RECORDER_DOING_NOTHING"></a><a id="recorder_doing_nothing"></a><dl>
<dt><b>RECORDER_DOING_NOTHING</b></dt>
</dl>
</td>
<td width="60%">
0x0

</td>
</tr>
<tr>
<td width="40%"><a id="RECORDER_OPENED"></a><a id="recorder_opened"></a><dl>
<dt><b>RECORDER_OPENED</b></dt>
</dl>
</td>
<td width="60%">
0x1

</td>
</tr>
</table>

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>