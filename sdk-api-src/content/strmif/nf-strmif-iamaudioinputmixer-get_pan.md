---
UID: NF:strmif.IAMAudioInputMixer.get_Pan
title: IAMAudioInputMixer::get_Pan
author: windows-sdk-content
description: The get_Pan method retrieves the pan level.
old-location: dshow\iamaudioinputmixer_get_pan.htm
tech.root: DirectShow
ms.assetid: aa1aae16-484e-4f78-901e-2fdb0d8e365c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Pan method, IAMAudioInputMixer.get_Pan, IAMAudioInputMixer::get_Pan, IAMAudioInputMixerget_Pan, dshow.iamaudioinputmixer_get_pan, get_Pan, get_Pan method [DirectShow], get_Pan method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Pan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioInputMixer.get_Pan
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMAudioInputMixer.get_Pan
: 
---

# IAMAudioInputMixer::get_Pan


## -description



The <code>get_Pan</code> method retrieves the pan level.




## -parameters




### -param pPan [out]

Receives the pan level. Possible values range from from –1.0 to 1.0, as follows:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>-1</td>
<td>Full left</td>
</tr>
<tr>
<td>0</td>
<td>Center</td>
</tr>
<tr>
<td>1</td>
<td>Full right</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/eb0528e0-81d0-45a3-831a-8cf3ff1232b6">IAMAudioInputMixer::put_Pan</a>
 

 

