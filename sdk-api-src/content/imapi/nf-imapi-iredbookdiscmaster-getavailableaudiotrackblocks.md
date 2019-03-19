---
UID: NF:imapi.IRedbookDiscMaster.GetAvailableAudioTrackBlocks
title: IRedbookDiscMaster::GetAvailableAudioTrackBlocks (imapi.h)
author: windows-sdk-content
description: Retrieves the current number of blocks that can be added to the track before an additional add will cause a failure for lack of space.
old-location: imapi\iredbookdiscmaster_getavailableaudiotrackblocks.htm
tech.root: imapi
ms.assetid: 57647490-0384-4cdb-842f-f1fb16dd2096
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAvailableAudioTrackBlocks, GetAvailableAudioTrackBlocks method [IMAPI], GetAvailableAudioTrackBlocks method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetAvailableAudioTrackBlocks method, IRedbookDiscMaster.GetAvailableAudioTrackBlocks, IRedbookDiscMaster::GetAvailableAudioTrackBlocks, _win32_iredbookdiscmaster_getavailableaudiotrackblocks, base.iredbookdiscmaster_getavailableaudiotrackblocks, imapi.iredbookdiscmaster_getavailableaudiotrackblocks, imapi/IRedbookDiscMaster::GetAvailableAudioTrackBlocks
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IRedbookDiscMaster.GetAvailableAudioTrackBlocks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRedbookDiscMaster::GetAvailableAudioTrackBlocks


## -description


Retrieves the current number of blocks that can be added to the track before an additional add will cause a failure for lack of space.


## -parameters




### -param pnBlocks [out]

Number of audio blocks that can be added to the open track before it must be closed.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



This method accounts for gaps associated with open tracks. Additionally, if this method is called when there is no open track, it returns the maximum number of audio blocks that could be added if a new track is created (accounting for gaps, and so on).




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

