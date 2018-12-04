---
UID: NF:mfidl.IMFTranscodeProfile.SetVideoAttributes
title: IMFTranscodeProfile::SetVideoAttributes
author: windows-sdk-content
description: Sets video stream configuration settings in the transcode profile.
old-location: mf\imftranscodeprofile_setvideoattributes.htm
tech.root: medfound
ms.assetid: e68653c5-5663-4839-a482-2244e147f4b9
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetVideoAttributes method, IMFTranscodeProfile.SetVideoAttributes, IMFTranscodeProfile::SetVideoAttributes, SetVideoAttributes, SetVideoAttributes method [Media Foundation], SetVideoAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setvideoattributes, mfidl/IMFTranscodeProfile::SetVideoAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMFTranscodeProfile.SetVideoAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile::SetVideoAttributes


## -description


Sets video stream configuration settings  in the transcode profile.

 For example code, see <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>.


## -parameters




### -param pAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store that contains contains the configuration settings for the video stream. The specified attribute values overwrites any existing values stored in the transcode profile. 

The following video attributes can be set:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
</li>
<li>
<a href="https://msdn.microsoft.com/73f23aed-d1b9-4821-b1ca-0a07f02b6913">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a6b6402-ff53-4399-8616-06b7768a8737">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/872140e8-fd39-446c-a84f-1e04ea95076e">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
</ul>
To create the attribute store, call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> methods depending on the data type of the attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

