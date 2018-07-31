---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetLoggingUrlCount
title: IWMReaderNetworkConfig::GetLoggingUrlCount
author: windows-sdk-content
description: The GetLoggingUrlCount method retrieves the number of URLs in the current list of logging URLs.
old-location: wmformat\iwmreadernetworkconfig_getloggingurlcount.htm
old-project: wmformat
ms.assetid: 869e093f-8936-4b60-8818-ee2c57924d11
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLoggingUrlCount, GetLoggingUrlCount method [windows Media Format], GetLoggingUrlCount method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetLoggingUrlCount method, IWMReaderNetworkConfig.GetLoggingUrlCount, IWMReaderNetworkConfig::GetLoggingUrlCount, IWMReaderNetworkConfigGetLoggingUrlCount, wmformat.iwmreadernetworkconfig_getloggingurlcount, wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrlCount
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
 - IWMReaderNetworkConfig.GetLoggingUrlCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetLoggingUrlCount


## -description



The <b>GetLoggingUrlCount</b> method retrieves the number of URLs in the current list of logging URLs.




## -parameters




### -param pdwUrlCount [out]

Pointer to a <b>DWORD</b> containing the URL count.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/27c5a97b-e04b-4d15-b19a-3c0d78feee95">IWMReaderNetworkConfig::GetLoggingUrl</a>
 

 

