---
UID: NF:imapi2.IRawCDImageTrackInfo.get_ISRC
title: IRawCDImageTrackInfo::get_ISRC
author: windows-sdk-content
description: Retrieves the International Standard Recording Code (ISRC) currently associated with the track. This property value defaults to NULL (or a zero-length string) and may only be set for tracks containing audio data.
old-location: imapi\irawcdimagetrackinfo_get_isrc.htm
tech.root: imapi
ms.assetid: 7e498391-37c6-4ac5-8d36-f3752ad5c4a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRawCDImageTrackInfo interface [IMAPI],get_ISRC method, IRawCDImageTrackInfo.get_ISRC, IRawCDImageTrackInfo::get_ISRC, get_ISRC, get_ISRC method [IMAPI], get_ISRC method [IMAPI],IRawCDImageTrackInfo interface, imapi.irawcdimagetrackinfo_get_isrc, imapi2/IRawCDImageTrackInfo::get_ISRC
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
 - IRawCDImageTrackInfo.get_ISRC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageTrackInfo::get_ISRC


## -description


Retrieves the International Standard Recording Code (ISRC) currently associated with the track.  This property value defaults to <b>NULL</b> (or a zero-length string) and may only be set for tracks containing audio data. 


## -parameters




### -param value [out, optional]

The ISRC currently associated with the track.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



  The format of the ISRC is provided to the caller formatted per ISRC standards (DIN-31-621) recommendations, such as "US-K7Y-98-12345".  When set, the provided string may optionally exclude all the '-' characters.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

