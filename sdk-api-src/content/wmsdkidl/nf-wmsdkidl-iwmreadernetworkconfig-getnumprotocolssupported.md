---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetNumProtocolsSupported
title: IWMReaderNetworkConfig::GetNumProtocolsSupported
author: windows-sdk-content
description: The GetNumProtocolsSupported method retrieves the number of supported protocols.
old-location: wmformat\iwmreadernetworkconfig_getnumprotocolssupported.htm
old-project: wmformat
ms.assetid: 6e249d8f-0351-452f-9b53-86f77df2fd70
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetNumProtocolsSupported, GetNumProtocolsSupported method [windows Media Format], GetNumProtocolsSupported method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetNumProtocolsSupported method, IWMReaderNetworkConfig.GetNumProtocolsSupported, IWMReaderNetworkConfig::GetNumProtocolsSupported, IWMReaderNetworkConfigGetNumProtocolsSupported, wmformat.iwmreadernetworkconfig_getnumprotocolssupported, wmsdkidl/IWMReaderNetworkConfig::GetNumProtocolsSupported
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
-	IWMReaderNetworkConfig.GetNumProtocolsSupported
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetNumProtocolsSupported


## -description



The <b>GetNumProtocolsSupported</b> method retrieves the number of supported protocols.




## -parameters




### -param pcProtocols [out]

Pointer to a count of the protocols.


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



Use this method along with <a href="https://msdn.microsoft.com/056d5f3f-79bf-4e21-9f2c-cda05eaca13d">IWMReaderAdvanced2::GetProtocolName</a> to iterate through the network protocols supported by the reader.

This method counts the number of protocols that the reader can use when receiving a stream. It does not indicate the protocols that are available for sending a stream.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>
 

 

