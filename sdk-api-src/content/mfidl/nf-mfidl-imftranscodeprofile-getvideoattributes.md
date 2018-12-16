---
UID: NF:mfidl.IMFTranscodeProfile.GetVideoAttributes
title: IMFTranscodeProfile::GetVideoAttributes
author: windows-sdk-content
description: Gets the video stream settings that are currently set in the transcode profile.
old-location: mf\imftranscodeprofile_getvideoattributes.htm
tech.root: medfound
ms.assetid: 734cb4d0-7017-4a30-9d0c-a6b5ce42fec6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVideoAttributes, GetVideoAttributes method [Media Foundation], GetVideoAttributes method [Media Foundation],IMFTranscodeProfile interface, IMFTranscodeProfile interface [Media Foundation],GetVideoAttributes method, IMFTranscodeProfile.GetVideoAttributes, IMFTranscodeProfile::GetVideoAttributes, mf.imftranscodeprofile_getvideoattributes, mfidl/IMFTranscodeProfile::GetVideoAttributes
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeProfile.GetVideoAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile::GetVideoAttributes


## -description


Gets the video stream settings that are currently set in the transcode profile.


## -parameters




### -param ppAttrs [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store containing the current video stream settings. Caller must release the interface pointer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If there are no container attributes set in the transcode profile, the <b>GetVideoAttributes</b> method  succeeds and  <i>ppAttrs</i> receives <b>NULL</b>.

To get a specific attribute value, the caller must call the appropriate <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> method depending on the data type of the attribute, and specify the attribute name. The following list shows the video attributes:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a6b6402-ff53-4399-8616-06b7768a8737">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/872140e8-fd39-446c-a84f-1e04ea95076e">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
<li>
<a href="https://msdn.microsoft.com/73f23aed-d1b9-4821-b1ca-0a07f02b6913">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

