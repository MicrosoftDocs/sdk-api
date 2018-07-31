---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.AddLoggingUrl
title: IWMReaderNetworkConfig::AddLoggingUrl
author: windows-sdk-content
description: The AddLoggingUrl method specifies a server that receive logging information from the reader object.
old-location: wmformat\iwmreadernetworkconfig_addloggingurl.htm
old-project: wmformat
ms.assetid: 471b17c8-20e4-44f3-88ee-48a35cd8930c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AddLoggingUrl, AddLoggingUrl method [windows Media Format], AddLoggingUrl method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],AddLoggingUrl method, IWMReaderNetworkConfig.AddLoggingUrl, IWMReaderNetworkConfig::AddLoggingUrl, IWMReaderNetworkConfigAddLoggingUrl, wmformat.iwmreadernetworkconfig_addloggingurl, wmsdkidl/IWMReaderNetworkConfig::AddLoggingUrl
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
 - IWMReaderNetworkConfig.AddLoggingUrl
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::AddLoggingUrl


## -description



The <b>AddLoggingUrl</b> method specifies a server that receive logging information from the reader object.




## -parameters




### -param pwszUrl [in]

Specifies a string containing the URL.


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
Null value passed in to <i>pwszUrl</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to create or add the URL.

</td>
</tr>
</table>
 




## -remarks



When the reader streams content from a server, it automatically sends logging information to that server. Use the <b>AddLoggingUrl</b> method to specify additional servers that will receive the logging information.




## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>
 

 

