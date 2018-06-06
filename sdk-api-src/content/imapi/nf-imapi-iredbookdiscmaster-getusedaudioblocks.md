---
UID: NF:imapi.IRedbookDiscMaster.GetUsedAudioBlocks
title: IRedbookDiscMaster::GetUsedAudioBlocks
author: windows-sdk-content
description: Retrieves the total number of audio blocks in use.
old-location: imapi\iredbookdiscmaster_getusedaudioblocks.htm
old-project: imapi
ms.assetid: 32921d7f-9cb2-4ae4-9064-18df91a237ba
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetUsedAudioBlocks, GetUsedAudioBlocks method [IMAPI], GetUsedAudioBlocks method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetUsedAudioBlocks method, IRedbookDiscMaster.GetUsedAudioBlocks, IRedbookDiscMaster::GetUsedAudioBlocks, _win32_iredbookdiscmaster_getusedaudioblocks, base.iredbookdiscmaster_getusedaudioblocks, imapi.iredbookdiscmaster_getusedaudioblocks, imapi/IRedbookDiscMaster::GetUsedAudioBlocks
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IRedbookDiscMaster.GetUsedAudioBlocks
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IRedbookDiscMaster::GetUsedAudioBlocks


## -description


Retrieves the total number of audio blocks in use.


## -parameters




### -param pnBlocks [out]

Total number of blocks in use, in both closed and open tracks.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

