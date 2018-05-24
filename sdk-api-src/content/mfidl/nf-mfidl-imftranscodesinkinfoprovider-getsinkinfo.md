---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.GetSinkInfo
title: IMFTranscodeSinkInfoProvider::GetSinkInfo
author: windows-driver-content
description: Gets the media types for the audio and video streams specified in the transcode profile.
old-location: mf\imftranscodesinkinfoprovider_getsinkinfo.htm
old-project: medfound
ms.assetid: d880e13a-879e-4882-a69d-f1920225e478
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetSinkInfo, GetSinkInfo method [Media Foundation], GetSinkInfo method [Media Foundation],IMFTranscodeSinkInfoProvider interface, IMFTranscodeSinkInfoProvider interface [Media Foundation],GetSinkInfo method, IMFTranscodeSinkInfoProvider.GetSinkInfo, IMFTranscodeSinkInfoProvider::GetSinkInfo, mf.imftranscodesinkinfoprovider_getsinkinfo, mfidl/IMFTranscodeSinkInfoProvider::GetSinkInfo
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFTranscodeSinkInfoProvider.GetSinkInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTranscodeSinkInfoProvider::GetSinkInfo


## -description



    Gets the media types for the audio and video streams specified in the transcode profile.


## -parameters




### -param pSinkInfo [out]

A pointer to an <a href="https://msdn.microsoft.com/b8f66128-88d5-4fe0-99f3-59621080be5c">MF_TRANSCODE_SINK_INFO</a> structure.

If the method succeeds, the method assigns <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> pointers to the <b>pAudioMediaType</b> and <b>pVideoMediaType</b> members of this structure. The method might set either member to <b>NULL</b>. If either member is non-NULL after the method returns, the caller must release the <b>IMFMediaType</b> pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this method, call <a href="https://msdn.microsoft.com/81137d8c-70b2-4a0a-a1b4-16a2f50f134b">IMFTranscodeSinkInfoProvider::SetProfile</a> to set the transcode profile. The <b>GetSinkInfo</b> method  uses the profile to create media types for the audio and video streams. 




## -see-also




<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile Interface</a>



<a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a>
 

 

