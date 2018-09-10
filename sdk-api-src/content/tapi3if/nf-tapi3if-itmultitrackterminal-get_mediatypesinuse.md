---
UID: NF:tapi3if.ITMultiTrackTerminal.get_MediaTypesInUse
title: ITMultiTrackTerminal::get_MediaTypesInUse
author: windows-sdk-content
description: The get_MediaTypesInUse method returns the media types (bitwise ORed) of all tracks managed currently by the multitrack terminal.
old-location: tapi3\itmultitrackterminal_get_mediatypesinuse.htm
tech.root: tapi
ms.assetid: 0c2ebbba-66a4-4ef0-abba-faab129e64e2
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_MediaTypesInUse method, ITMultiTrackTerminal.get_MediaTypesInUse, ITMultiTrackTerminal::get_MediaTypesInUse, _tapi3_itmultitrackterminal_get_mediatypesinuse, get_MediaTypesInUse, get_MediaTypesInUse method [TAPI 2.2], get_MediaTypesInUse method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_mediatypesinuse, tapi3if/ITMultiTrackTerminal::get_MediaTypesInUse
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITMultiTrackTerminal.get_MediaTypesInUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMultiTrackTerminal::get_MediaTypesInUse


## -description


The 
<b>get_MediaTypesInUse</b> method returns the media types (bitwise ORed) of all tracks managed currently by the multitrack terminal. For tracks that are multitrack terminals themselves, this method calls the track's <b>ITMultiTrackTerminal::get_MediaTypesInUse</b> method to determine the track's media types.


## -parameters




### -param plMediaTypesInUse [out]

Bitwise ORed list of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> in use.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>
 

 

