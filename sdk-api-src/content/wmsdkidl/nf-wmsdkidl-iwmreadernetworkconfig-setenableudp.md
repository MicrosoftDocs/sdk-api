---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetEnableUDP
title: IWMReaderNetworkConfig::SetEnableUDP
author: windows-sdk-content
description: The SetEnableUDP method enables or disables UDP.
old-location: wmformat\iwmreadernetworkconfig_setenableudp.htm
tech.root: wmformat
ms.assetid: 03afdef3-2aa8-4826-8dce-6d501fa42bcd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetEnableUDP method, IWMReaderNetworkConfig.SetEnableUDP, IWMReaderNetworkConfig::SetEnableUDP, IWMReaderNetworkConfigSetEnableUDP, SetEnableUDP, SetEnableUDP method [windows Media Format], SetEnableUDP method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setenableudp, wmsdkidl/IWMReaderNetworkConfig::SetEnableUDP
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
 - IWMReaderNetworkConfig.SetEnableUDP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::SetEnableUDP


## -description



The <b>SetEnableUDP</b> method enables or disables UDP.




## -parameters




### -param fEnableUDP [in]

Boolean value that is True if UDP is to be enabled. Set this to true if the reader can use UDP-based MMS streaming when selecting a protocol for streaming.


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
 




## -remarks



This setting applies only to a protocol rollover or MMS://URL. Even if this setting is disabled, the application can still specify an explicit MMSU://URL and stream MMS via TCP successfully.

For more information, see the Remarks section of <a href="https://msdn.microsoft.com/en-us/library/Dd743538(v=VS.85).aspx">IWMReaderNetworkConfig::ResetProtocolRollover</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743524(v=VS.85).aspx">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743525(v=VS.85).aspx">IWMReaderNetworkConfig::GetEnableUDP</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743543(v=VS.85).aspx">IWMReaderNetworkConfig::SetEnableTCP</a>
 

 

