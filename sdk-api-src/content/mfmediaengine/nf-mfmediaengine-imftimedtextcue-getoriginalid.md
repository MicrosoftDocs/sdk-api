---
UID: NF:mfmediaengine.IMFTimedTextCue.GetOriginalId
title: IMFTimedTextCue::GetOriginalId
author: windows-sdk-content
description: Gets the cue identifier that is provided in the text-track data format, if available.
old-location: mf\imftimedtextcue_getoriginalid.htm
tech.root: medfound
ms.assetid: D5B94171-AEB0-4A7D-B596-F888B69A436D
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetOriginalId, GetOriginalId method [Media Foundation], GetOriginalId method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetOriginalId method, IMFTimedTextCue.GetOriginalId, IMFTimedTextCue::GetOriginalId, mf.imftimedtextcue_getoriginalid, mfmediaengine/IMFTimedTextCue::GetOriginalId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
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
req.lib: Mfmediaengine.lib
req.dll: Mfmediaengine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.dll
api_name:
 - IMFTimedTextCue.GetOriginalId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfmediaengine.h
: 
- IMFTimedTextCue.GetOriginalId
: 
---

# IMFTimedTextCue::GetOriginalId


## -description


Gets the cue identifier that is provided in the text-track data format, if available.


## -parameters




### -param originalId [out]

Type: <b>LPWSTR*</b>

The cue identifier that is provided in the text-track data format.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves an identifier for the cue that is included in the source data, if one was specified. The system dynamically generates identifiers for cues that are guaranteed to be unique within a single time-text track. To obtain this system-generated ID, call <a href="https://msdn.microsoft.com/D096B1FA-E92F-4B09-9177-13203FF1704D">GetId</a>.




## -see-also




<a href="https://msdn.microsoft.com/D096B1FA-E92F-4B09-9177-13203FF1704D">GetId</a>



<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

