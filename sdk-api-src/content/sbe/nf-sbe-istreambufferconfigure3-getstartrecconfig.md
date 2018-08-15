---
UID: NF:sbe.IStreamBufferConfigure3.GetStartRecConfig
title: IStreamBufferConfigure3::GetStartRecConfig
author: windows-sdk-content
description: The GetStartRecConfig method queries whether the IStreamBufferRecordControl::Start method automatically stops the current recording.
old-location: mstv\istreambufferconfigure3_getstartrecconfig.htm
old-project: mstv
ms.assetid: caf50c08-5247-4229-8952-9d538362b33d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetStartRecConfig, GetStartRecConfig method [Microsoft TV Technologies], GetStartRecConfig method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, IStreamBufferConfigure3 interface [Microsoft TV Technologies],GetStartRecConfig method, IStreamBufferConfigure3.GetStartRecConfig, IStreamBufferConfigure3::GetStartRecConfig, IStreamBufferConfigure3GetStartRecConfig, mstv.istreambufferconfigure3_getstartrecconfig, sbe/IStreamBufferConfigure3::GetStartRecConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure3.GetStartRecConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferConfigure3::GetStartRecConfig


## -description


The <b>GetStartRecConfig</b> method queries whether the <a href="https://msdn.microsoft.com/e72ec34e-d3e3-4f5f-9336-d55135dc1e47">IStreamBufferRecordControl::Start</a> method automatically stops the current recording.


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




<a href="https://msdn.microsoft.com/73f3cd43-11d1-4eff-861d-087bfda7d135">IStreamBufferConfigure3 Interface</a>
 

 

