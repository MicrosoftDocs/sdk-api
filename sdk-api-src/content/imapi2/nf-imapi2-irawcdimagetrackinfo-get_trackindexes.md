---
UID: NF:imapi2.IRawCDImageTrackInfo.get_TrackIndexes
title: IRawCDImageTrackInfo::get_TrackIndexes
author: windows-sdk-content
description: Retrieves the one-based index of the tracks on the disc.
old-location: imapi\irawcdimagetrackinfo_get_trackindexes.htm
tech.root: imapi
ms.assetid: a83766f7-8d02-47df-9691-26d6f2cd0d5b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_TrackIndexes method, IRawCDImageTrackInfo.get_TrackIndexes, IRawCDImageTrackInfo::get_TrackIndexes, get_TrackIndexes, get_TrackIndexes method [IMAPI], get_TrackIndexes method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_trackindexes, imapi2/IRawCDImageTrackInfo::get_TrackIndexes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo.get_TrackIndexes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageTrackInfo::get_TrackIndexes


## -description


Retrieves the one-based index of the tracks on the disc.


## -parameters




### -param value [out]

The one-based index associated with this track.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

