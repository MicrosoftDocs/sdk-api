---
UID: NF:evr.IMFVideoMixerControl2.GetMixingPrefs
title: IMFVideoMixerControl2::GetMixingPrefs
author: windows-sdk-content
description: Gets the current preferences for video deinterlacing.
old-location: mf\imfvideomixercontrol2_getmixingprefs.htm
old-project: medfound
ms.assetid: 4ec03db2-9e7f-4a11-8d69-7654391a33d8
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetMixingPrefs, GetMixingPrefs method [Media Foundation], GetMixingPrefs method [Media Foundation],IMFVideoMixerControl2 interface, IMFVideoMixerControl2 interface [Media Foundation],GetMixingPrefs method, IMFVideoMixerControl2.GetMixingPrefs, IMFVideoMixerControl2::GetMixingPrefs, evr/IMFVideoMixerControl2::GetMixingPrefs, mf.imfvideomixercontrol2_getmixingprefs
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IMFVideoMixerControl2.GetMixingPrefs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoMixerControl2::GetMixingPrefs


## -description


Gets the current preferences for video deinterlacing.


## -parameters




### -param pdwMixFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/28dcc8b1-684e-4178-9606-118e77d8ff58">MFVideoMixPrefs</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a238b050-101d-4b8a-9479-984b889823f4">IMFVideoMixerControl2</a>



<a href="https://msdn.microsoft.com/3617adf2-ed7b-4788-abce-58bc22a14511">Video Quality Management</a>
 

 

