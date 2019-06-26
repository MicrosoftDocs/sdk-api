---
UID: NF:mfidl.IMFAudioPolicy.GetGroupingParam
title: IMFAudioPolicy::GetGroupingParam (mfidl.h)
author: windows-sdk-content
description: Retrieves the group of sessions to which this audio session belongs.
old-location: mf\imfaudiopolicy_getgroupingparam.htm
tech.root: medfound
ms.assetid: 725892fd-4af6-483d-bb5c-87051fa45ec4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 725892fd-4af6-483d-bb5c-87051fa45ec4, GetGroupingParam, GetGroupingParam method [Media Foundation], GetGroupingParam method [Media Foundation],IMFAudioPolicy interface, IMFAudioPolicy interface [Media Foundation],GetGroupingParam method, IMFAudioPolicy.GetGroupingParam, IMFAudioPolicy::GetGroupingParam, mf.imfaudiopolicy_getgroupingparam, mfidl/IMFAudioPolicy::GetGroupingParam
ms.topic: method
f1_keywords: 
 - "mfidl/IMFAudioPolicy.GetGroupingParam"
req.header: mfidl.h
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
 - IMFAudioPolicy.GetGroupingParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAudioPolicy::GetGroupingParam


## -description



Retrieves the group of sessions to which this audio session belongs.




## -parameters




### -param pguidClass [out]

Receives a GUID that identifies the session group.


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



If two or more audio sessions share the same group, the Windows volume control displays one slider control for the entire group. Otherwise, it displays a slider for each session. For more information, see <b>IAudioSessionControl::SetGroupingParam</b> in the core audio API documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy">IMFAudioPolicy</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>
 

 

