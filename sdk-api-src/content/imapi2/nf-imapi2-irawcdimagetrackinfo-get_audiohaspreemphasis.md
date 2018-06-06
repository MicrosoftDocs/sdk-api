---
UID: NF:imapi2.IRawCDImageTrackInfo.get_AudioHasPreemphasis
title: IRawCDImageTrackInfo::get_AudioHasPreemphasis
author: windows-sdk-content
description: Retrieves the value that specifies if an audio track has an additional pre-emphasis added to the audio data.
old-location: imapi\irawcdimagetrackinfo_get_audiohaspreemphasis.htm
old-project: imapi
ms.assetid: 3e322485-4542-4229-9b3e-17c9774d14b5
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_AudioHasPreemphasis method, IRawCDImageTrackInfo.get_AudioHasPreemphasis, IRawCDImageTrackInfo::get_AudioHasPreemphasis, get_AudioHasPreemphasis, get_AudioHasPreemphasis method [IMAPI], get_AudioHasPreemphasis method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_audiohaspreemphasis, imapi2/IRawCDImageTrackInfo::get_AudioHasPreemphasis
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo.get_AudioHasPreemphasis
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IRawCDImageTrackInfo::get_AudioHasPreemphasis


## -description


Retrieves  the value that specifies if an audio track has an additional pre-emphasis added to the audio data.


## -parameters




### -param value [out]

Value that specifies if an audio track has an additional pre-emphasis added to the audio data.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

