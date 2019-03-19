---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableUDP
title: IWMReaderNetworkConfig::GetEnableUDP (wmsdkidl.h)
author: windows-sdk-content
description: The GetEnableUDP method queries whether UDP is enabled for protocol rollover.
old-location: wmformat\iwmreadernetworkconfig_getenableudp.htm
tech.root: wmformat
ms.assetid: 81c6536c-303c-4eac-a75a-54e9df29e299
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnableUDP, GetEnableUDP method [windows Media Format], GetEnableUDP method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableUDP method, IWMReaderNetworkConfig.GetEnableUDP, IWMReaderNetworkConfig::GetEnableUDP, IWMReaderNetworkConfigGetEnableUDP, wmformat.iwmreadernetworkconfig_getenableudp, wmsdkidl/IWMReaderNetworkConfig::GetEnableUDP
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
 - IWMReaderNetworkConfig.GetEnableUDP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::GetEnableUDP


## -description



The <b>GetEnableUDP</b> method queries whether <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">UDP</a> is enabled for protocol rollover.




## -parameters




### -param pfEnableUDP [out]

Pointer to a variable that receives a Boolean value. If the value is <b>TRUE</b>, the reader object includes UDP when it performs protocol rollover. If the value is FASLE, the reader does not use UDP for protocol rollover. However, the reader will still use UDP if the URL explicitly specifies a UDP-based protocol, such as MMSU or RTSPU.


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
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743524(v=VS.85).aspx">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743543(v=VS.85).aspx">IWMReaderNetworkConfig::SetEnableTCP</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743544(v=VS.85).aspx">IWMReaderNetworkConfig::SetEnableUDP</a>
 

 

