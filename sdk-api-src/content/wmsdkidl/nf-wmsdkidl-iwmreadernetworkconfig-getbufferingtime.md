---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetBufferingTime
title: IWMReaderNetworkConfig::GetBufferingTime
author: windows-sdk-content
description: The GetBufferingTime method retrieves the amount of time that the network source buffers data before rendering it.
old-location: wmformat\iwmreadernetworkconfig_getbufferingtime.htm
tech.root: wmformat
ms.assetid: a3f35230-363c-48e7-bef9-b92e0b50b978
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetBufferingTime, GetBufferingTime method [windows Media Format], GetBufferingTime method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetBufferingTime method, IWMReaderNetworkConfig.GetBufferingTime, IWMReaderNetworkConfig::GetBufferingTime, IWMReaderNetworkConfigGetBufferingTime, wmformat.iwmreadernetworkconfig_getbufferingtime, wmsdkidl/IWMReaderNetworkConfig::GetBufferingTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderNetworkConfig.GetBufferingTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::GetBufferingTime


## -description



The <b>GetBufferingTime</b> method retrieves the amount of time that the network source buffers data before rendering it.




## -parameters




### -param pcnsBufferingTime [out]

Pointer to a variable that receives the buffering time, in 100-nanosecond units.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL passed in to <i>pcnsBufferingTime</i>

</td>
</tr>
</table>
 




## -remarks



See the Remarks for <a href="https://msdn.microsoft.com/64b8eb13-3b96-4bb7-8d75-0eccb1af5a2f">SetBufferingTime</a>.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/64b8eb13-3b96-4bb7-8d75-0eccb1af5a2f">IWMReaderNetworkConfig::SetBufferingTime</a>
 

 

