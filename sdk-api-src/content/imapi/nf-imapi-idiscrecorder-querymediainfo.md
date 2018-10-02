---
UID: NF:imapi.IDiscRecorder.QueryMediaInfo
title: IDiscRecorder::QueryMediaInfo
author: windows-sdk-content
description: Retrieves information about the currently mounted media, such as the total number of blocks used on the media.
old-location: imapi\idiscrecorder_querymediainfo.htm
tech.root: imapi
ms.assetid: 5e97d5e5-1a10-4ef2-b083-427d4070283f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDiscRecorder interface [IMAPI],QueryMediaInfo method, IDiscRecorder.QueryMediaInfo, IDiscRecorder::QueryMediaInfo, QueryMediaInfo, QueryMediaInfo method [IMAPI], QueryMediaInfo method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_querymediainfo, base.idiscrecorder_querymediainfo, imapi.idiscrecorder_querymediainfo, imapi/IDiscRecorder::QueryMediaInfo
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
 - IDiscRecorder.QueryMediaInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder::QueryMediaInfo


## -description


Retrieves information about the currently mounted media, such as the total number of blocks used on the media.


## -parameters




### -param pbSessions

TBD


### -param pbLastTrack

TBD


### -param ulStartAddress

TBD


### -param ulNextWritable

TBD


### -param ulFreeBlocks

TBD




#### - pblasttrack [out]

Track number of the last track of the previous session.


#### - pbsessions [out]

Number of sessions on the disc.


#### - ulfreeblocks [out]

Number of blocks available for writing.


#### - ulnextwritable [out]

Address at which writing is to begin.


#### - ulstartaddress [out]

Start address of the last track of the previous session.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Using this method allows the calculation of parameters such as the amount of free space left on the disc without using a setting on the active disc recorder, which causes an exclusive open. The total size of the disc can be calculated by summing the next writable address and free blocks.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

