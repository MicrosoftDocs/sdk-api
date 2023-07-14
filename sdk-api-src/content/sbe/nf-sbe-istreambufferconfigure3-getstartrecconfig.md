---
UID: NF:sbe.IStreamBufferConfigure3.GetStartRecConfig
title: IStreamBufferConfigure3::GetStartRecConfig (sbe.h)
description: The GetStartRecConfig method queries whether the IStreamBufferRecordControl::Start method automatically stops the current recording.
helpviewer_keywords: ["GetStartRecConfig","GetStartRecConfig method [Microsoft TV Technologies]","GetStartRecConfig method [Microsoft TV Technologies]","IStreamBufferConfigure3 interface","IStreamBufferConfigure3 interface [Microsoft TV Technologies]","GetStartRecConfig method","IStreamBufferConfigure3.GetStartRecConfig","IStreamBufferConfigure3::GetStartRecConfig","IStreamBufferConfigure3GetStartRecConfig","mstv.istreambufferconfigure3_getstartrecconfig","sbe/IStreamBufferConfigure3::GetStartRecConfig"]
old-location: mstv\istreambufferconfigure3_getstartrecconfig.htm
tech.root: mstv
ms.assetid: caf50c08-5247-4229-8952-9d538362b33d
ms.date: 12/05/2018
ms.keywords: GetStartRecConfig, GetStartRecConfig method [Microsoft TV Technologies], GetStartRecConfig method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, IStreamBufferConfigure3 interface [Microsoft TV Technologies],GetStartRecConfig method, IStreamBufferConfigure3.GetStartRecConfig, IStreamBufferConfigure3::GetStartRecConfig, IStreamBufferConfigure3GetStartRecConfig, mstv.istreambufferconfigure3_getstartrecconfig, sbe/IStreamBufferConfigure3::GetStartRecConfig
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
 - IStreamBufferConfigure3::GetStartRecConfig
 - sbe/IStreamBufferConfigure3::GetStartRecConfig
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
 - IStreamBufferConfigure3.GetStartRecConfig
---

# IStreamBufferConfigure3::GetStartRecConfig


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetStartRecConfig</b> method queries whether the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordcontrol-start">IStreamBufferRecordControl::Start</a> method automatically stops the current recording.

## -parameters

### -param pfStartStopsCur [out]

Receives a Boolean value. If <b>TRUE</b>, the <b>Start</b> method automatically stops the current recording. Otherwise, the <b>Start</b> method fails if another recording is in progress.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure3">IStreamBufferConfigure3 Interface</a>