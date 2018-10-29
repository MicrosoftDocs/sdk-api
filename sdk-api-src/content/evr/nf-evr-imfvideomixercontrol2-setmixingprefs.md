---
UID: NF:evr.IMFVideoMixerControl2.SetMixingPrefs
title: IMFVideoMixerControl2::SetMixingPrefs
author: windows-sdk-content
description: Sets the preferences for video deinterlacing.
old-location: mf\imfvideomixercontrol2_setmixingprefs.htm
tech.root: medfound
ms.assetid: ae8fa85a-bdae-4fbf-b9d4-a987eb1c4c41
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFVideoMixerControl2 interface [Media Foundation],SetMixingPrefs method, IMFVideoMixerControl2.SetMixingPrefs, IMFVideoMixerControl2::SetMixingPrefs, SetMixingPrefs, SetMixingPrefs method [Media Foundation], SetMixingPrefs method [Media Foundation],IMFVideoMixerControl2 interface, evr/IMFVideoMixerControl2::SetMixingPrefs, mf.imfvideomixercontrol2_setmixingprefs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: evr.h
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
 - evr.h
api_name:
 - IMFVideoMixerControl2.SetMixingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoMixerControl2::SetMixingPrefs


## -description


Sets the preferences for video deinterlacing.


## -parameters




### -param dwMixFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/28dcc8b1-684e-4178-9606-118e77d8ff58">MFVideoMixPrefs</a> enumeration.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a238b050-101d-4b8a-9479-984b889823f4">IMFVideoMixerControl2</a>



<a href="https://msdn.microsoft.com/3617adf2-ed7b-4788-abce-58bc22a14511">Video Quality Management</a>
 

 

