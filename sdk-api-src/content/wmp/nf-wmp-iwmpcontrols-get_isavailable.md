---
UID: NF:wmp.IWMPControls.get_isAvailable
title: IWMPControls::get_isAvailable
author: windows-sdk-content
description: The get_isAvailable method indicates whether a specified type of information is available or a specified action can be performed.
old-location: wmp\iwmpcontrols_get_isavailable.htm
tech.root: WMP
ms.assetid: 702e09f2-e086-45e3-9ae1-b62ec3e9561f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPControls interface [Windows Media Player],get_isAvailable method, IWMPControls.get_isAvailable, IWMPControls::get_isAvailable, IWMPControlsget_isAvailable, get_isAvailable, get_isAvailable method [Windows Media Player], get_isAvailable method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_get_isavailable, wmp/IWMPControls::get_isAvailable
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
 - IWMPControls.get_isAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls::get_isAvailable


## -description



The <b>get_isAvailable</b> method indicates whether a specified type of information is available or a specified action can be performed.




## -parameters




### -param bstrItem [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>currentItem</td>
<td>Determines whether the user can set the <b>IWMPControls::put_currentItem</b> method.</td>
</tr>
<tr>
<td>currentMarker</td>
<td>Determines whether the user can seek to a specific marker.</td>
</tr>
<tr>
<td>currentPosition</td>
<td>Determines whether the user can seek to a specific position in the file. Some files do not support seeking.</td>
</tr>
<tr>
<td>fastForward</td>
<td>Determines whether the file supports fast forwarding and whether that functionality can be invoked. Many file types (or live streams) do not support fastForward.</td>
</tr>
<tr>
<td>fastReverse</td>
<td>Determines whether the file supports fastReverse and whether that functionality can be invoked. Many file types (or live streams) do not support fastReverse.</td>
</tr>
<tr>
<td>next</td>
<td>Determines whether the user can seek to the next entry in a playlist.</td>
</tr>
<tr>
<td>pause</td>
<td>Determines whether the <b>IWMPControls::pause</b> method is available.</td>
</tr>
<tr>
<td>play</td>
<td>Determines whether the <b>IWMPControls::play</b> method is available.</td>
</tr>
<tr>
<td>previous</td>
<td>Determines whether the user can seek to the previous entry in a playlist.</td>
</tr>
<tr>
<td>step</td>
<td>Determines whether the <b>IWMPControls2::step</b> method is available during playback.</td>
</tr>
<tr>
<td>stop</td>
<td>Determines whether the <b>IWMPControls::stop</b> method is available.</td>
</tr>
</table>
 


### -param pIsAvailable [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether a specified type of information is available or a specified action can be performed.


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




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/d54a4bb7-855f-4807-89b5-176b7fac2edd">IWMPControls2::step</a>



<a href="https://msdn.microsoft.com/ef8a3f0e-b424-43ab-bb42-83e9f80f5d19">IWMPControls::pause</a>



<a href="https://msdn.microsoft.com/45b5634b-6d23-4e61-90e4-ef0cc9d90a14">IWMPControls::play</a>



<a href="https://msdn.microsoft.com/190cec53-5cd9-4bd0-b8d9-23c5389fe231">IWMPControls::put_currentItem</a>



<a href="https://msdn.microsoft.com/97ab009d-5ad9-4049-a212-1ef95941f951">IWMPControls::stop</a>
 

 

