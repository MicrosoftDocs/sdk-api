---
UID: NF:tapi3if.ITPhone.get_RingVolume
title: ITPhone::get_RingVolume
author: windows-sdk-content
description: The get_RingVolume method retrieves the current ring volume for the phone.
old-location: tapi3\itphone_get_ringvolume.htm
tech.root: tapi
ms.assetid: 147553f1-74a7-4f80-bbf3-b140d9b375ba
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_RingVolume method, ITPhone.get_RingVolume, ITPhone::get_RingVolume, _tapi3_itphone_get_ringvolume, get_RingVolume, get_RingVolume method [TAPI 2.2], get_RingVolume method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_ringvolume, tapi3if/ITPhone::get_RingVolume
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
 - ITPhone.get_RingVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_RingVolume


## -description


The 
<b>get_RingVolume</b> method retrieves the current ring volume for the phone.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param plRingVolume [out]

Ring volume.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/858ca6a8-a53b-4858-b4b0-985230ec8ea0">put_RingVolume</a>
 

 

