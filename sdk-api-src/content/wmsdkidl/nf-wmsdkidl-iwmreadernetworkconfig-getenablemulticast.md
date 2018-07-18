---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetEnableMulticast
title: IWMReaderNetworkConfig::GetEnableMulticast
author: windows-sdk-content
description: The GetEnableMulticast method ascertains whether multicast is enabled.
old-location: wmformat\iwmreadernetworkconfig_getenablemulticast.htm
old-project: wmformat
ms.assetid: 2fc51a74-18b6-4ddd-9089-9a8bdfce70ea
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetEnableMulticast, GetEnableMulticast method [windows Media Format], GetEnableMulticast method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetEnableMulticast method, IWMReaderNetworkConfig.GetEnableMulticast, IWMReaderNetworkConfig::GetEnableMulticast, IWMReaderNetworkConfigGetEnableMulticast, wmformat.iwmreadernetworkconfig_getenablemulticast, wmsdkidl/IWMReaderNetworkConfig::GetEnableMulticast
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/02e3a7cc-1dcf-4aba-a18f-2056742f0777">IWMReaderNetworkConfig::SetEnableMulticast</a>
 

 

