---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.SetProfile
title: IMFTranscodeSinkInfoProvider::SetProfile
author: windows-sdk-content
description: Sets the transcoding profile on the transcode sink activation object.
old-location: mf\imftranscodesinkinfoprovider_setprofile.htm
old-project: medfound
ms.assetid: 81137d8c-70b2-4a0a-a1b4-16a2f50f134b
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFTranscodeSinkInfoProvider interface [Media Foundation],SetProfile method, IMFTranscodeSinkInfoProvider.SetProfile, IMFTranscodeSinkInfoProvider::SetProfile, SetProfile, SetProfile method [Media Foundation], SetProfile method [Media Foundation],IMFTranscodeSinkInfoProvider interface, mf.imftranscodesinkinfoprovider_setprofile, mfidl/IMFTranscodeSinkInfoProvider::SetProfile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTranscodeSinkInfoProvider.SetProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

