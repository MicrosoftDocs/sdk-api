---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFTranscodeSinkInfoProvider::SetProfile


## -description


Sets the transcoding profile on the transcode sink activation object.


## -parameters




### -param pProfile [in]

A pointer to the <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> interface. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this method, initialize the profile object as follows:

<ul>
<li>Set the <a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a> attribute to specify the container type of the output file.</li>
<li>If the output file will have a video stream, set video attributes by calling the <a href="https://msdn.microsoft.com/e68653c5-5663-4839-a482-2244e147f4b9">IMFTranscodeProfile::SetVideoAttributes</a> method.</li>
<li>If the output file will have an audio stream, set audio attributes by calling the <a href="https://msdn.microsoft.com/4118bb2b-8373-434a-896b-de5a1ba8c793">IMFTranscodeProfile::SetAudioAttributes</a> method.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a>
 

 

