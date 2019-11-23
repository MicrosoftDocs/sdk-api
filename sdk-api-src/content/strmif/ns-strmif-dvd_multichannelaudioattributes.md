---
UID: NS:strmif.tagDVD_MultichannelAudioAttributes
title: DVD_MultichannelAudioAttributes (strmif.h)

description: The DVD_MultichannelAudioAttributes structure describes the multichannel attributes of one audio stream within a specified title.
old-location: dshow\dvd_multichannelaudioattributes.htm
tech.root: DirectShow
ms.assetid: 8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d

ms.date: 12/05/2018
ms.keywords: DVD_MultichannelAudioAttributes, DVD_MultichannelAudioAttributes structure [DirectShow], DVD_MultichannelAudioAttributesStructure, dshow.dvd_multichannelaudioattributes, strmif/DVD_MultichannelAudioAttributes
ms.topic: struct
f1_keywords: 
 - "strmif/DVD_MultichannelAudioAttributes"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_MultichannelAudioAttributes
targetos: Windows
req.typenames: DVD_MultichannelAudioAttributes
req.redist: 
ms.custom: 19H1
---

# DVD_MultichannelAudioAttributes structure


## -description



The <code>DVD_MultichannelAudioAttributes</code> structure describes the multichannel attributes of one audio stream within a specified title.




## -struct-fields




### -field Info

Array of eight <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_mua_mixinginfo">DVD_MUA_MixingInfo</a> structures, which contain the mixing information for each channel in the audio stream.


### -field Coeff

Array of eight <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_mua_coeff">DVD_MUA_Coeff</a> structures, which contain the mixing coefficients for each channel in the audio stream.


## -remarks



The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_titleattributes">DVD_TitleAttributes</a> structure contains an array of up to eight <b>DVD_MultichannelAudioAttributes</b> structures. When <code>DVD_TitleAttributes</code> is filled by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a> method, the array will be populated with one <b>DVD_MultichannelAudioAttributes</b> structure for each available audio stream in the title.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

