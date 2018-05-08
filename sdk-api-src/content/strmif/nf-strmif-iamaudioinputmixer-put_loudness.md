---
UID: NF:strmif.IAMAudioInputMixer.put_Loudness
title: IAMAudioInputMixer::put_Loudness
author: windows-driver-content
description: The put_Loudness method enables or disables the loudness control.
old-location: dshow\iamaudioinputmixer_put_loudness.htm
old-project: DirectShow
ms.assetid: e4baca46-260c-45fe-8c03-304c906aab15
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Loudness method, IAMAudioInputMixer.put_Loudness, IAMAudioInputMixer::put_Loudness, IAMAudioInputMixerput_Loudness, dshow.iamaudioinputmixer_put_loudness, put_Loudness, put_Loudness method [DirectShow], put_Loudness method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Loudness
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMAudioInputMixer.put_Loudness
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioInputMixer::put_Loudness


## -description



The <code>put_Loudness</code> method enables or disables the loudness control.




## -parameters




### -param fLoudness [in]

Specifies whether loudness is on or off. Use one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Sets loudness on.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Sets loudness off.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Loudness boosts the bass of low volume signals before they are recorded, to compensate for the fact that the ear does not hear quiet bass sounds as well as other sounds.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/620003c0-401f-4415-a82f-a80e7b32dbd3">IAMAudioInputMixer::get_Loudness</a>
 

 

