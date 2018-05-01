---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
title: IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection method
author: windows-driver-content
description: The SetForceRerunAutoProxyDetection method enables or disables forced rerun detection.
old-location: wmformat\iwmreadernetworkconfig_setforcererunautoproxydetection.htm
old-project: wmformat
ms.assetid: 3c84fc2a-5933-45da-a7a3-728a8837d851
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], SetForceRerunAutoProxyDetection method, IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection, IWMReaderNetworkConfigSetForceRerunAutoProxyDetection, SetForceRerunAutoProxyDetection method [windows Media Format], SetForceRerunAutoProxyDetection method [windows Media Format], IWMReaderNetworkConfig interface, SetForceRerunAutoProxyDetection,IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection, wmformat.iwmreadernetworkconfig_setforcererunautoproxydetection, wmsdkidl/IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection method


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

Setting <i>fForceRerunDetection</i> to True applies to all protocols when the auto setting has been specified by the <a href="https://msdn.microsoft.com/fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2">SetProxySettings</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/af4c4f4d-ad19-46b5-b38f-9aa51f2d95ba">IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection</a>
 

 

