---
UID: NF:wmcontainer.IMFASFSplitter.GetLastSendTime
title: IMFASFSplitter::GetLastSendTime (wmcontainer.h)
author: windows-sdk-content
description: Retrieves the send time of the last sample received.
old-location: mf\imfasfsplitter_getlastsendtime.htm
tech.root: medfound
ms.assetid: 59a6c53c-2cdf-4677-a5a3-4138f107f721
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 59a6c53c-2cdf-4677-a5a3-4138f107f721, GetLastSendTime, GetLastSendTime method [Media Foundation], GetLastSendTime method [Media Foundation],IMFASFSplitter interface, IMFASFSplitter interface [Media Foundation],GetLastSendTime method, IMFASFSplitter.GetLastSendTime, IMFASFSplitter::GetLastSendTime, mf.imfasfsplitter_getlastsendtime, wmcontainer/IMFASFSplitter::GetLastSendTime
ms.topic: method
f1_keywords: 
 - "wmcontainer/IMFASFSplitter.GetLastSendTime"
dev_langs:
 - c++
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.GetLastSendTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFSplitter::GetLastSendTime


## -description



Retrieves the send time of the last sample received.




## -parameters




### -param pdwLastSendTime [out]

Receives the send time of the last sample received.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwLastSendTime</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags">IMFASFSplitter::SetFlags</a>
 

 

