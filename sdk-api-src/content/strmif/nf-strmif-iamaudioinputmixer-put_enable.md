---
UID: NF:strmif.IAMAudioInputMixer.put_Enable
title: IAMAudioInputMixer::put_Enable
author: windows-sdk-content
description: The put_Enable method enables or disables an input.
old-location: dshow\iamaudioinputmixer_put_enable.htm
old-project: DirectShow
ms.assetid: 84f179bf-2e2f-4ba0-81b7-c20acd09ccea
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMAudioInputMixer interface [DirectShow],put_Enable method, IAMAudioInputMixer.put_Enable, IAMAudioInputMixer::put_Enable, IAMAudioInputMixerput_Enable, dshow.iamaudioinputmixer_put_enable, put_Enable, put_Enable method [DirectShow], put_Enable method [DirectShow],IAMAudioInputMixer interface, strmif/IAMAudioInputMixer::put_Enable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAudioInputMixer.put_Enable
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAudioInputMixer::put_Enable


## -description



The <code>put_Enable</code> method enables or disables an input.




## -parameters




### -param fEnable [in]

Specifies whether to enable or disable the input. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Enable the input.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Disable the input.</td>
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
</table>
 




## -remarks



If an input is enabled, it is mixed into the recorded signal.

This method applies to specific input pins on the <a href="https://msdn.microsoft.com/f76d5c82-33b2-4579-9420-8f97eca53ede">Audio Capture Filter</a>, so the filter itself returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/217cb49d-7f5f-42c5-83db-546621f6a375">IAMAudioInputMixer Interface</a>



<a href="https://msdn.microsoft.com/d3ec509c-9990-4803-a4e3-abc88fc8c522">IAMAudioInputMixer::get_Enable</a>
 

 

