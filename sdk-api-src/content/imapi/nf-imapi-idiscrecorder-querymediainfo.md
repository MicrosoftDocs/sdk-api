---
UID: NF:imapi.IDiscRecorder.QueryMediaInfo
title: IDiscRecorder::QueryMediaInfo (imapi.h)
description: Retrieves information about the currently mounted media, such as the total number of blocks used on the media.
helpviewer_keywords: ["IDiscRecorder interface [IMAPI]","QueryMediaInfo method","IDiscRecorder.QueryMediaInfo","IDiscRecorder::QueryMediaInfo","QueryMediaInfo","QueryMediaInfo method [IMAPI]","QueryMediaInfo method [IMAPI]","IDiscRecorder interface","_win32_idiscrecorder_querymediainfo","base.idiscrecorder_querymediainfo","imapi.idiscrecorder_querymediainfo","imapi/IDiscRecorder::QueryMediaInfo"]
old-location: imapi\idiscrecorder_querymediainfo.htm
tech.root: imapi
ms.assetid: 5e97d5e5-1a10-4ef2-b083-427d4070283f
ms.date: 12/05/2018
ms.keywords: IDiscRecorder interface [IMAPI],QueryMediaInfo method, IDiscRecorder.QueryMediaInfo, IDiscRecorder::QueryMediaInfo, QueryMediaInfo, QueryMediaInfo method [IMAPI], QueryMediaInfo method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_querymediainfo, base.idiscrecorder_querymediainfo, imapi.idiscrecorder_querymediainfo, imapi/IDiscRecorder::QueryMediaInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder::QueryMediaInfo
 - imapi/IDiscRecorder::QueryMediaInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.QueryMediaInfo
---

# IDiscRecorder::QueryMediaInfo


## -description

Retrieves information about the currently mounted media, such as the total number of blocks used on the media.

## -parameters

### -param pbSessions [out]

Number of sessions on the disc.

### -param pbLastTrack [out]

Track number of the last track of the previous session.

### -param ulStartAddress [out]

Start address of the last track of the previous session.

### -param ulNextWritable [out]

Address at which writing is to begin.

### -param ulFreeBlocks [out]

Number of blocks available for writing.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

Using this method allows the calculation of parameters such as the amount of free space left on the disc without using a setting on the active disc recorder, which causes an exclusive open. The total size of the disc can be calculated by summing the next writable address and free blocks.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>