---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetEnableTCP
title: IWMReaderNetworkConfig::SetEnableTCP
author: windows-sdk-content
description: The SetEnableTCP method enables or disables TCP.
old-location: wmformat\iwmreadernetworkconfig_setenabletcp.htm
old-project: wmformat
ms.assetid: 8afc62b8-a2f6-4470-8005-804e0980b599
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetEnableTCP method, IWMReaderNetworkConfig.SetEnableTCP, IWMReaderNetworkConfig::SetEnableTCP, IWMReaderNetworkConfigSetEnableTCP, SetEnableTCP, SetEnableTCP method [windows Media Format], SetEnableTCP method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setenabletcp, wmsdkidl/IWMReaderNetworkConfig::SetEnableTCP
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
 - IWMReaderNetworkConfig.SetEnableTCP
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetEnableTCP


## -description



The <b>SetEnableTCP</b> method enables or disables TCP.




## -parameters




### -param fEnableTCP [in]

Boolean value that is True if TCP is to be enabled. Set this to true if the SDK can use TCP-based MMS streaming when selecting a protocol for streaming.


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



This setting applies only to a protocol rollover or MMS://URL. Even if this setting is disabled, the application can still specify an explicit MMST://URL and stream MMS via TCP successfully.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/6623c2f9-24cb-4038-9aa5-2eb634b3f1a2">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="https://msdn.microsoft.com/81c6536c-303c-4eac-a75a-54e9df29e299">IWMReaderNetworkConfig::GetEnableUDP</a>



<a href="https://msdn.microsoft.com/03afdef3-2aa8-4826-8dce-6d501fa42bcd">IWMReaderNetworkConfig::SetEnableUDP</a>
 

 

