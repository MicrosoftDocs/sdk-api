---
UID: NF:imapi2.IRawCDImageTrackInfo.put_DigitalAudioCopySetting
title: IRawCDImageTrackInfo::put_DigitalAudioCopySetting (imapi2.h)
description: Sets the digital audio copy &quot;Allowed&quot; bit to one of three values on the resulting media. Please see the IMAPI_CD_TRACK_DIGITAL_COPY_SETTING enumeration for additional information on each possible value.
helpviewer_keywords: ["IRawCDImageTrackInfo interface [IMAPI]","put_DigitalAudioCopySetting method","IRawCDImageTrackInfo.put_DigitalAudioCopySetting","IRawCDImageTrackInfo::put_DigitalAudioCopySetting","imapi.irawcdimagetrackinfo_put_digitalaudiocopysetting","imapi2/IRawCDImageTrackInfo::put_DigitalAudioCopySetting","put_DigitalAudioCopySetting","put_DigitalAudioCopySetting method [IMAPI]","put_DigitalAudioCopySetting method [IMAPI]","IRawCDImageTrackInfo interface"]
old-location: imapi\irawcdimagetrackinfo_put_digitalaudiocopysetting.htm
tech.root: imapi
ms.assetid: 48d00305-4dc4-432c-80b7-955bbcdb3cc2
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],put_DigitalAudioCopySetting method, IRawCDImageTrackInfo.put_DigitalAudioCopySetting, IRawCDImageTrackInfo::put_DigitalAudioCopySetting, imapi.irawcdimagetrackinfo_put_digitalaudiocopysetting, imapi2/IRawCDImageTrackInfo::put_DigitalAudioCopySetting, put_DigitalAudioCopySetting, put_DigitalAudioCopySetting method [IMAPI], put_DigitalAudioCopySetting method [IMAPI],IRawCDImageTrackInfo interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawCDImageTrackInfo::put_DigitalAudioCopySetting
 - imapi2/IRawCDImageTrackInfo::put_DigitalAudioCopySetting
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo.put_DigitalAudioCopySetting
---

# IRawCDImageTrackInfo::put_DigitalAudioCopySetting


## -description

Sets the digital audio copy  "Allowed" bit to one of three values on the resulting media.  Please see the <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_track_digital_copy_setting">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a> enumeration for additional information on each possible value.

## -parameters

### -param value [in]

The digital audio copy setting value to assign.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This property may only be set for tracks containing audio data.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_track_digital_copy_setting">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo">IRawCDImageTrackInfo</a>