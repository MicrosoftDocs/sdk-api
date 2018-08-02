---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetBufferingTime
title: IWMReaderNetworkConfig::SetBufferingTime
author: windows-sdk-content
description: The SetBufferingTime method specifies how long the network source buffers data before rendering it.
old-location: wmformat\iwmreadernetworkconfig_setbufferingtime.htm
old-project: wmformat
ms.assetid: 64b8eb13-3b96-4bb7-8d75-0eccb1af5a2f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetBufferingTime method, IWMReaderNetworkConfig.SetBufferingTime, IWMReaderNetworkConfig::SetBufferingTime, IWMReaderNetworkConfigSetBufferingTime, SetBufferingTime, SetBufferingTime method [windows Media Format], SetBufferingTime method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setbufferingtime, wmsdkidl/IWMReaderNetworkConfig::SetBufferingTime
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
 - IWMReaderNetworkConfig.SetBufferingTime
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetBufferingTime


## -description



The <b>SetBufferingTime</b> method specifies how long the network source buffers data before rendering it.




## -parameters




### -param cnsBufferingTime [in]

Specifies the amount of time in to buffer content before starting playback, in 100-nanosecond units.


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
<i>cnsBufferingTime</i> is larger than the maximum or smaller than the minimum.

</td>
</tr>
</table>
 




## -remarks



The minimum buffering time is 1 second and the maximum is 60 seconds. To set a buffering time of 1 second, for example, set the value to 10000000.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/a3f35230-363c-48e7-bef9-b92e0b50b978">IWMReaderNetworkConfig::GetBufferingTime</a>
 

 

