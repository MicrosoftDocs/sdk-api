---
UID: NF:audioendpoints.IAudioEndpointFormatControl.ResetToDefault
title: IAudioEndpointFormatControl::ResetToDefault
author: windows-sdk-content
description: Resets the format to the default setting provided by the device manufacturer.
old-location: coreaudio\iaudioendpointformatcontrol_resettodefault.htm
old-project: CoreAudio
ms.assetid: EAE5206D-8BDF-4016-A0E6-D56D0F6B3566
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IAudioEndpointFormatControl interface [Core Audio],ResetToDefault method, IAudioEndpointFormatControl.ResetToDefault, IAudioEndpointFormatControl::ResetToDefault, ResetToDefault, ResetToDefault method [Core Audio], ResetToDefault method [Core Audio],IAudioEndpointFormatControl interface, audioendpoints/IAudioEndpointFormatControl::ResetToDefault, coreaudio.iaudioendpointformatcontrol_resettodefault
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioendpoints.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
tech.root: 
req.typenames: AudioClientProperties
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AudioEndpoints.h
api_name:
 - IAudioEndpointFormatControl.ResetToDefault
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointFormatControl::ResetToDefault


## -description


Resets the format to the default setting provided by the device manufacturer.


## -parameters




### -param ResetFlags [in]

Allows the application to specify which formats are reset.  If
                      no flags are set, then this method reevaluates both the endpoint's 
    device format and mix format and sets them to their default values.

ENDPOINT_FORMAT_RESET_MIX_ONLY: Only reset the mix format.  The endpoint's device
    format will not be reset if this flag is set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7FF7DCF2-0580-4B50-8EA9-87DB9478B1E8">IAudioEndpointFormatControl</a>
 

 

