---
UID: NF:sbe.IStreamBufferConfigure3.SetStartRecConfig
title: IStreamBufferConfigure3::SetStartRecConfig (sbe.h)
description: The SetStartRecConfig method specifies whether the IStreamBufferRecordControl::Start method automatically stops the current recording.
helpviewer_keywords: ["IStreamBufferConfigure3 interface [Microsoft TV Technologies]","SetStartRecConfig method","IStreamBufferConfigure3.SetStartRecConfig","IStreamBufferConfigure3::SetStartRecConfig","IStreamBufferConfigure3SetStartRecConfig","SetStartRecConfig","SetStartRecConfig method [Microsoft TV Technologies]","SetStartRecConfig method [Microsoft TV Technologies]","IStreamBufferConfigure3 interface","mstv.istreambufferconfigure3_setstartrecconfig","sbe/IStreamBufferConfigure3::SetStartRecConfig"]
old-location: mstv\istreambufferconfigure3_setstartrecconfig.htm
tech.root: mstv
ms.assetid: 6ae896ce-72e8-49aa-a538-2a269ef07ade
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure3 interface [Microsoft TV Technologies],SetStartRecConfig method, IStreamBufferConfigure3.SetStartRecConfig, IStreamBufferConfigure3::SetStartRecConfig, IStreamBufferConfigure3SetStartRecConfig, SetStartRecConfig, SetStartRecConfig method [Microsoft TV Technologies], SetStartRecConfig method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, mstv.istreambufferconfigure3_setstartrecconfig, sbe/IStreamBufferConfigure3::SetStartRecConfig
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IStreamBufferConfigure3::SetStartRecConfig
 - sbe/IStreamBufferConfigure3::SetStartRecConfig
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
 - IStreamBufferConfigure3.SetStartRecConfig
---

# IStreamBufferConfigure3::SetStartRecConfig


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetStartRecConfig</b> method specifies whether the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">IStreamBufferRecordControl::Start</a> method automatically stops the current recording.

## -parameters

### -param fStartStopsCur [in]

If <b>TRUE</b>, the <b>Start</b> method automatically stops the current recording. Otherwise, the <b>Start</b> method fails if another recording is in progress. The default value is <b>FALSE</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

By default, if another recording is still in progress, the <b>IStreamBufferRecordControl::Start</b> method fails. If the <i>fStartStopsCur</i> parameter is <b>TRUE</b>, the <b>Start</b> method will automatically stop a recording in progress.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure3">IStreamBufferConfigure3 Interface</a>