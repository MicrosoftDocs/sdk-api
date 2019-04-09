---
UID: NF:imapi2.IRawCDImageTrackInfo.put_DigitalAudioCopySetting
title: IRawCDImageTrackInfo::put_DigitalAudioCopySetting (imapi2.h)
author: windows-sdk-content
description: Sets the digital audio copy &#0034;Allowed&#0034; bit to one of three values on the resulting media. Please see the IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration for additional information on each possible value.
old-location: imapi\irawcdimagetrackinfo_put_digitalaudiocopysetting.htm
tech.root: imapi
ms.assetid: 48d00305-4dc4-432c-80b7-955bbcdb3cc2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],put_DigitalAudioCopySetting method, IRawCDImageTrackInfo.put_DigitalAudioCopySetting, IRawCDImageTrackInfo::put_DigitalAudioCopySetting, imapi.irawcdimagetrackinfo_put_digitalaudiocopysetting, imapi2/IRawCDImageTrackInfo::put_DigitalAudioCopySetting, put_DigitalAudioCopySetting, put_DigitalAudioCopySetting method [IMAPI], put_DigitalAudioCopySetting method [IMAPI],IRawCDImageTrackInfo interface
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo.put_DigitalAudioCopySetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageTrackInfo::put_DigitalAudioCopySetting


## -description


Sets the digital audio copy  "Allowed" bit to one of three values on the resulting media.  Please see the <a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a> enumeration for additional information on each possible value.


## -parameters




### -param value [in]

The digital audio copy setting value to assign.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This property may only be set for tracks containing audio data.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a>



<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

