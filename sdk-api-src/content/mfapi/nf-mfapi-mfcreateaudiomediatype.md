---
UID: NF:mfapi.MFCreateAudioMediaType
title: MFCreateAudioMediaType function
author: windows-sdk-content
description: Creates an audio media type from a WAVEFORMATEX structure.
old-location: mf\mfcreateaudiomediatype.htm
tech.root: medfound
ms.assetid: 8857e150-1746-4f3f-aaa8-db0f44787621
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 8857e150-1746-4f3f-aaa8-db0f44787621, MFCreateAudioMediaType, MFCreateAudioMediaType function [Media Foundation], mf.mfcreateaudiomediatype, mfapi/MFCreateAudioMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateAudioMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateAudioMediaType function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future.]

Creates an audio media type from a <b>WAVEFORMATEX</b> structure.


## -parameters




### -param pAudioFormat [in]

Pointer to a <b>WAVEFORMATEX</b> structure that describes the audio format.


### -param ppIAudioMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/425a4a37-6fd3-4724-9d18-c39cc2862ef7">IMFAudioMediaType</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/425a4a37-6fd3-4724-9d18-c39cc2862ef7">IMFAudioMediaType</a> interface is deprecrated, so applications should avoid using this function. To create a media type from a <b>WAVEFORMATEX</b> structure, do the following:
      

<ol>
<li>Call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>. This function returns a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The returned media type object is initially empty.
          </li>
<li>Call <a href="https://msdn.microsoft.com/91a201a6-06cf-4445-ad62-fdabb3848d51">MFInitMediaTypeFromWaveFormatEx</a> to populate the media type from the <b>WAVEFORMATEX</b> structure.
          </li>
</ol>
Alternatively, you can call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a> and then set the media type attributes directly.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/15aad4ea-7b4b-4a6f-bac7-18e0c281f2a6">Audio Media Types</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

