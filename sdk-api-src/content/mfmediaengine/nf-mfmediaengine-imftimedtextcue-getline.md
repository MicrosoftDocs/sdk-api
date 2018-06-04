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

# IMFTimedTextCue::GetLine


## -description


Gets a line of text in the cue from the index of the line.


## -parameters




### -param index




### -param line






#### - nIndex [in]

Type: <b>DWORD</b>

The index of the line of text in the cue to retrieve.




#### - ppLine [out]

Type: <b><a href="https://msdn.microsoft.com/98327CA2-21C4-481F-B979-12C31AA1E7B2">IMFTimedTextFormattedText</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/98327CA2-21C4-481F-B979-12C31AA1E7B2">IMFTimedTextFormattedText</a> interface for the line of text in the cue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

