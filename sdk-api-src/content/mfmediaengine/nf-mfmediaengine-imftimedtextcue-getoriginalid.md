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

# IMFTimedTextCue::GetOriginalId


## -description


Gets the cue identifier that is provided in the text-track data format, if available.


## -parameters




### -param originalId [out]

Type: <b>LPWSTR*</b>

The cue identifier that is provided in the text-track data format.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves an identifier for the cue that is included in the source data, if one was specified. The system dynamically generates identifiers for cues that are guaranteed to be unique within a single time-text track. To obtain this system-generated ID, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetId</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetId</a>



<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

