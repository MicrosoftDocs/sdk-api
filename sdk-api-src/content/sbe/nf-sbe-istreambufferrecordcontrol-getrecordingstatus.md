---
UID: NF:sbe.IStreamBufferRecordControl.GetRecordingStatus
title: IStreamBufferRecordControl::GetRecordingStatus (sbe.h)
description: The GetRecordingStatus method retrieves the status of the recording.
helpviewer_keywords: ["GetRecordingStatus","GetRecordingStatus method [Microsoft TV Technologies]","GetRecordingStatus method [Microsoft TV Technologies]","IStreamBufferRecordControl interface","IStreamBufferRecordControl interface [Microsoft TV Technologies]","GetRecordingStatus method","IStreamBufferRecordControl.GetRecordingStatus","IStreamBufferRecordControl::GetRecordingStatus","IStreamBufferRecordControlGetRecordingStatus","mstv.istreambufferrecordcontrol_getrecordingstatus","sbe/IStreamBufferRecordControl::GetRecordingStatus"]
old-location: mstv\istreambufferrecordcontrol_getrecordingstatus.htm
tech.root: mstv
ms.assetid: 313f2ad0-7401-4a36-a229-abfc67737324
ms.date: 12/05/2018
ms.keywords: GetRecordingStatus, GetRecordingStatus method [Microsoft TV Technologies], GetRecordingStatus method [Microsoft TV Technologies],IStreamBufferRecordControl interface, IStreamBufferRecordControl interface [Microsoft TV Technologies],GetRecordingStatus method, IStreamBufferRecordControl.GetRecordingStatus, IStreamBufferRecordControl::GetRecordingStatus, IStreamBufferRecordControlGetRecordingStatus, mstv.istreambufferrecordcontrol_getrecordingstatus, sbe/IStreamBufferRecordControl::GetRecordingStatus
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IStreamBufferRecordControl::GetRecordingStatus
 - sbe/IStreamBufferRecordControl::GetRecordingStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecordControl.GetRecordingStatus
---

# IStreamBufferRecordControl::GetRecordingStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetRecordingStatus</b> method retrieves the status of the recording.

## -parameters

### -param phResult [out]

Pointer to a variable that receives an <b>HRESULT</b> value. The <b>HRESULT</b> value indicates the current status of writing or closing the file. This parameter can be <b>NULL</b>.

### -param pbStarted [out]

Pointer to a variable that receives a Boolean value, indicating whether the recording has started,

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The recording has started.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The recording has not started.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.

### -param pbStopped [out]

Pointer to a variable that receives a Boolean value, indicating whether recording has been stopped.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The recording has stopped.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The recording has not stopped, or has not started yet.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method reports the status of the <b>Start</b> and <b>Stop</b> methods, which themselves are asynchronous.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordcontrol">IStreamBufferRecordControl Interface</a>