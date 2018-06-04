---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMSyncReader2::SetRangeByTimecode


## -description



The <b>SetRangeByTimecode</b> method sets a starting and ending time, based on SMPTE time codes, for playback of a file.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number.


### -param pStart [in]

Pointer to a <a href="https://msdn.microsoft.com/039c352c-d1f0-443f-acef-f730e949725c">WMT_TIMECODE_EXTENSION_DATA</a> structure containing the starting time code.


### -param pEnd [in]

Pointer to a <b>WMT_TIMECODE_EXTENSION_DATA</b> structure containing the ending time code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



For the method to succeed, the file must be indexed by SMPTE time code.

If the call is successful, all streams are synchronized to the same position based on presentation time.




## -see-also




<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>
 

 

