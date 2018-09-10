---
UID: NF:strmif.IAMAudioInputMixer.get_Enable
title: IAMAudioInputMixer::get_Enable
author: windows-sdk-content
description: The get_Enable method retrieves whether the input is enabled.
old-location: dshow\iamaudioinputmixer_get_enable.htm
tech.root: DirectShow
ms.assetid: d3ec509c-9990-4803-a4e3-abc88fc8c522
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],get_Enable method, IAMAudioInputMixer.get_Enable, IAMAudioInputMixer::get_Enable, IAMAudioInputMixerget_Enable, dshow.iamaudioinputmixer_get_enable, get_Enable, get_Enable method [DirectShow], get_Enable method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::get_Enable
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
 - IAMAudioInputMixer.get_Enable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAudioInputMixer::get_Enable


## -description



The <code>get_Enable</code> method retrieves whether the input is enabled.




## -parameters




### -param pfEnable [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Input is enabled.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Input is disabled.</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method applies to specific input pins on the <a href="https://msdn.microsoft.com/f76d5c82-33b2-4579-9420-8f97eca53ede">Audio Capture Filter</a>, so the filter itself returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/84f179bf-2e2f-4ba0-81b7-c20acd09ccea">IAMAudioInputMixer::put_Enable</a>
 

 

