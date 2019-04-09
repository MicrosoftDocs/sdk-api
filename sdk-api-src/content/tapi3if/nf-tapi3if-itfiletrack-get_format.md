---
UID: NF:tapi3if.ITFileTrack.get_Format
title: ITFileTrack::get_Format (tapi3if.h)
author: windows-sdk-content
description: The get_Format method gets the file terminal's format.
old-location: tapi3\itfiletrack_get_format.htm
tech.root: Tapi
ms.assetid: 6d489888-49b3-4fcd-9643-82f0a08fe1c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITFileTrack interface [TAPI 2.2],get_Format method, ITFileTrack.get_Format, ITFileTrack::get_Format, _tapi3_itfiletrack_get_format, get_Format, get_Format method [TAPI 2.2], get_Format method [TAPI 2.2],ITFileTrack interface, tapi3.itfiletrack_get_format, tapi3if/ITFileTrack::get_Format
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITFileTrack.get_Format
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITFileTrack::get_Format


## -description


The 
<b>get_Format</b> method gets the file terminal's format.


## -parameters




### -param ppmt [out]

Pointer to an 
<b>AM_MEDIA_TYPE</b> descriptor of the terminal format. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/590ca1ea-e058-4238-b01c-249fddd3c87d">ITFileTrack</a>
 

 

