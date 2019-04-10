---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
title: IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection (wmsdkidl.h)
author: windows-sdk-content
description: The SetForceRerunAutoProxyDetection method enables or disables forced rerun detection.
old-location: wmformat\iwmreadernetworkconfig_setforcererunautoproxydetection.htm
tech.root: wmformat
ms.assetid: 3c84fc2a-5933-45da-a7a3-728a8837d851
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetForceRerunAutoProxyDetection method, IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection, IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection, IWMReaderNetworkConfigSetForceRerunAutoProxyDetection, SetForceRerunAutoProxyDetection, SetForceRerunAutoProxyDetection method [windows Media Format], SetForceRerunAutoProxyDetection method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setforcererunautoproxydetection, wmsdkidl/IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection
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
 - IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection


## -description



The <b>SetForceRerunAutoProxyDetection</b> method enables or disables forced rerun detection.




## -parameters




### -param fForceRerunDetection [in]

Boolean value that is True if forced rerun detection is to be enabled.


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



Forced rerun detection indicates that Web Proxy Auto-Detection mechanisms must be invoked before the next streaming connection is established.

Setting <i>fForceRerunDetection</i> to True applies to all protocols when the auto setting has been specified by the <a href="https://msdn.microsoft.com/en-us/library/Dd743550(v=VS.85).aspx">SetProxySettings</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743526(v=VS.85).aspx">IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection</a>
 

 

