---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableMulticast
title: IWMReaderNetworkConfig::GetEnableMulticast (wmsdkidl.h)
author: windows-sdk-content
description: The GetEnableMulticast method ascertains whether multicast is enabled.
old-location: wmformat\iwmreadernetworkconfig_getenablemulticast.htm
tech.root: wmformat
ms.assetid: 2fc51a74-18b6-4ddd-9089-9a8bdfce70ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEnableMulticast, GetEnableMulticast method [windows Media Format], GetEnableMulticast method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableMulticast method, IWMReaderNetworkConfig.GetEnableMulticast, IWMReaderNetworkConfig::GetEnableMulticast, IWMReaderNetworkConfigGetEnableMulticast, wmformat.iwmreadernetworkconfig_getenablemulticast, wmsdkidl/IWMReaderNetworkConfig::GetEnableMulticast
ms.topic: method
f1_keywords: 
 - "wmsdkidl/IWMReaderNetworkConfig.GetEnableMulticast"
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
 - IWMReaderNetworkConfig.GetEnableMulticast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig::GetEnableMulticast


## -description



The <b>GetEnableMulticast</b> method ascertains whether multicast is enabled.




## -parameters




### -param pfEnableMulticast [out]

Pointer to a Boolean value that is set to True if multicast has been enabled.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenablemulticast">IWMReaderNetworkConfig::SetEnableMulticast</a>
 

 

