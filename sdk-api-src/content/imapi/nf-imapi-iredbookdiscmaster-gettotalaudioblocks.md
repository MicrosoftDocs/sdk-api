---
UID: NF:imapi.IRedbookDiscMaster.GetTotalAudioBlocks
title: IRedbookDiscMaster::GetTotalAudioBlocks
author: windows-sdk-content
description: Retrieves the total number of blocks available for staging audio tracks. The total includes all block types, including blocks that may need to be allocated for track gaps.
old-location: imapi\iredbookdiscmaster_gettotalaudioblocks.htm
tech.root: imapi
ms.assetid: c4b0f02e-d881-4a4f-9356-d8232ef4c297
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetTotalAudioBlocks, GetTotalAudioBlocks method [IMAPI], GetTotalAudioBlocks method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetTotalAudioBlocks method, IRedbookDiscMaster.GetTotalAudioBlocks, IRedbookDiscMaster::GetTotalAudioBlocks, _win32_iredbookdiscmaster_gettotalaudioblocks, base.iredbookdiscmaster_gettotalaudioblocks, imapi.iredbookdiscmaster_gettotalaudioblocks, imapi/IRedbookDiscMaster::GetTotalAudioBlocks
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRedbookDiscMaster.GetTotalAudioBlocks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRedbookDiscMaster::GetTotalAudioBlocks


## -description


Retrieves the total number of blocks available for staging audio tracks. The total includes all block types, including blocks that may need to be allocated for track gaps.


## -parameters




### -param pnBlocks [out]

Total number of audio blocks available on a disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

