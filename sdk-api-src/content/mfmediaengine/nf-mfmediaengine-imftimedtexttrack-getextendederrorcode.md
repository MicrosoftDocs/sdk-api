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

# IMFTimedTextTrack::GetExtendedErrorCode


## -description


Gets the extended error code for the latest error associated with the track.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

The extended error code for the latest error associated with the track.




## -remarks



If the most recent error was associated with a track, this value will be the same <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a> as returned by the <a href="https://msdn.microsoft.com/3658EE26-497D-4D33-BE68-572BCE1B28B1">IMFTimedTextNotify::Error</a> method.




## -see-also




<a href="https://msdn.microsoft.com/55232D19-F3D0-42C7-8B24-C2A7768B2C7E">IMFTimedTextTrack</a>
 

 

