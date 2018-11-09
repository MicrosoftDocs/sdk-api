---
UID: NF:tapi3if.ITPhone.put_RingVolume
title: ITPhone::put_RingVolume
author: windows-sdk-content
description: The put_RingVolume method requests that the phone change its ring volume.
old-location: tapi3\itphone_put_ringvolume.htm
tech.root: tapi
ms.assetid: 858ca6a8-a53b-4858-b4b0-985230ec8ea0
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_RingVolume method, ITPhone.put_RingVolume, ITPhone::put_RingVolume, _tapi3_itphone_put_ringvolume, put_RingVolume, put_RingVolume method [TAPI 2.2], put_RingVolume method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_ringvolume, tapi3if/ITPhone::put_RingVolume
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
 - ITPhone.put_RingVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::put_RingVolume


## -description


The 
<b>put_RingVolume</b> method requests that the phone change its ring volume.

The application must call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.


## -parameters




### -param lRingVolume [in]

Phone volume. For more information, see the following Remarks section.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the phone is currently ringing (RingMode != 0), the new volume takes effect immediately. If the phone is not currently ringing (RingMode == 0), the new volume takes effect the next time the phone rings.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/147553f1-74a7-4f80-bbf3-b140d9b375ba">get_RingVolume</a>
 

 

