---
UID: NF:imapi.IRedbookDiscMaster.GetAudioBlockSize
title: IRedbookDiscMaster::GetAudioBlockSize
author: windows-sdk-content
description: Retrieves the size, in bytes, of an audio block.
old-location: imapi\iredbookdiscmaster_getaudioblocksize.htm
tech.root: imapi
ms.assetid: 25e8fd75-7a24-421f-b61e-b131dfbbcc8c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetAudioBlockSize, GetAudioBlockSize method [IMAPI], GetAudioBlockSize method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetAudioBlockSize method, IRedbookDiscMaster.GetAudioBlockSize, IRedbookDiscMaster::GetAudioBlockSize, _win32_iredbookdiscmaster_getaudioblocksize, base.iredbookdiscmaster_getaudioblocksize, imapi.iredbookdiscmaster_getaudioblocksize, imapi/IRedbookDiscMaster::GetAudioBlockSize
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
 - IRedbookDiscMaster.GetAudioBlockSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRedbookDiscMaster::GetAudioBlockSize


## -description


Retrieves the size, in bytes, of an audio block.


## -parameters




### -param pnBlockBytes [out]

Total size, in bytes, of a single audio block.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



This method returns 2352.




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

