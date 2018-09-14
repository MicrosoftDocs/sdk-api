---
UID: NF:wmp.IWMPSettings.getMode
title: IWMPSettings::getMode
author: windows-sdk-content
description: The getMode method determines whether the loop mode or shuffle mode is active.
old-location: wmp\iwmpsettings_getmode.htm
tech.root: WMP
ms.assetid: 5275cb99-8007-4af2-9137-694de18c5434
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPSettings interface [Windows Media Player],getMode method, IWMPSettings.getMode, IWMPSettings::getMode, IWMPSettingsgetMode, getMode, getMode method [Windows Media Player], getMode method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_getmode, wmp/IWMPSettings::getMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.getMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSettings::getMode


## -description



The <b>getMode</b> method determines whether the loop mode or shuffle mode is active.




## -parameters




### -param bstrMode [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>autoRewind</td>
<td>Tracks are restarted from the beginning after playing to the end.</td>
</tr>
<tr>
<td>loop</td>
<td>The sequence of tracks repeats itself.</td>
</tr>
<tr>
<td>showFrame</td>
<td>The nearest key frame is displayed when not playing. This mode is not relevant for audio tracks.</td>
</tr>
<tr>
<td>shuffle</td>
<td>Tracks are played in random order.</td>
</tr>
</table>
 


### -param pvarfMode [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the specified mode is active.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/28a404a7-5bb0-41bb-a5b2-cc6138b8176e">IWMPSettings::setMode</a>
 

 

