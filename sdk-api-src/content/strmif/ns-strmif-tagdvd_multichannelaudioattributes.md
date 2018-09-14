---
UID: NS:strmif.tagDVD_MultichannelAudioAttributes
title: tagDVD_MultichannelAudioAttributes
author: windows-sdk-content
description: The DVD_MultichannelAudioAttributes structure describes the multichannel attributes of one audio stream within a specified title.
old-location: dshow\dvd_multichannelaudioattributes.htm
tech.root: DirectShow
ms.assetid: 8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DVD_MultichannelAudioAttributes, DVD_MultichannelAudioAttributes structure [DirectShow], DVD_MultichannelAudioAttributesStructure, dshow.dvd_multichannelaudioattributes, strmif/DVD_MultichannelAudioAttributes, tagDVD_MultichannelAudioAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: DVD_MultichannelAudioAttributes
req.redist: 
---

# tagDVD_MultichannelAudioAttributes structure


## -description



The <code>DVD_MultichannelAudioAttributes</code> structure describes the multichannel attributes of one audio stream within a specified title.




## -struct-fields




### -field Info

Array of eight <a href="https://msdn.microsoft.com/df830598-f484-483d-a0dc-e6bd9debbe53">DVD_MUA_MixingInfo</a> structures, which contain the mixing information for each channel in the audio stream.


### -field Coeff

Array of eight <a href="https://msdn.microsoft.com/8b8402da-37c2-4983-ae09-967c269fc828">DVD_MUA_Coeff</a> structures, which contain the mixing coefficients for each channel in the audio stream.


## -remarks



The <a href="https://msdn.microsoft.com/e80baf09-93b7-4285-ac9a-af72cae137de">DVD_TitleAttributes</a> structure contains an array of up to eight <b>DVD_MultichannelAudioAttributes</b> structures. When <code>DVD_TitleAttributes</code> is filled by a call to the <a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a> method, the array will be populated with one <b>DVD_MultichannelAudioAttributes</b> structure for each available audio stream in the title.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

