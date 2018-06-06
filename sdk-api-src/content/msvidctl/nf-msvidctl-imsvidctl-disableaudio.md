---
UID: NF:msvidctl.IMSVidCtl.DisableAudio
title: IMSVidCtl::DisableAudio
author: windows-sdk-content
description: The DisableAudio method disables the audio output device.
old-location: mstv\imsvidctl_disableaudio.htm
old-project: mstv
ms.assetid: 0166cdc3-de1c-4505-855e-f69144cc71aa
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DisableAudio, DisableAudio method [Microsoft TV Technologies], DisableAudio method [Microsoft TV Technologies],IMSVidCtl interface, IMSVidCtl interface [Microsoft TV Technologies],DisableAudio method, IMSVidCtl.DisableAudio, IMSVidCtl::DisableAudio, IMSVidCtlDisableAudio, mstv.imsvidctl_disableaudio, msvidctl/IMSVidCtl::DisableAudio
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.DisableAudio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::DisableAudio


## -description


The <b>DisableAudio</b> method disables the audio output device.


## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method sets the active audio output device to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/1f6498ce-fb53-4d57-b6bd-6696ba57de3b">IMSVidCtl::put_AudioRendererActive</a>
 

 

