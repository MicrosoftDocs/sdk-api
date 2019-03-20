---
UID: NF:mfidl.IMFAudioPolicy.SetGroupingParam
title: IMFAudioPolicy::SetGroupingParam (mfidl.h)
author: windows-sdk-content
description: Assigns the audio session to a group of sessions.
old-location: mf\imfaudiopolicy_setgroupingparam.htm
tech.root: medfound
ms.assetid: 2c024208-f13f-4fd1-b5a8-b881af226670
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 2c024208-f13f-4fd1-b5a8-b881af226670, IMFAudioPolicy interface [Media Foundation],SetGroupingParam method, IMFAudioPolicy.SetGroupingParam, IMFAudioPolicy::SetGroupingParam, SetGroupingParam, SetGroupingParam method [Media Foundation], SetGroupingParam method [Media Foundation],IMFAudioPolicy interface, mf.imfaudiopolicy_setgroupingparam, mfidl/IMFAudioPolicy::SetGroupingParam
ms.topic: method
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
 - IMFAudioPolicy.SetGroupingParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioPolicy::SetGroupingParam


## -description



Assigns the audio session to a group of sessions.




## -parameters




### -param rguidClass [in]

A <b>GUID</b> that identifies the session group. Groups are application-defined. To create a new session group, assign a new GUID.


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




<a href="https://msdn.microsoft.com/fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a">IMFAudioPolicy</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

