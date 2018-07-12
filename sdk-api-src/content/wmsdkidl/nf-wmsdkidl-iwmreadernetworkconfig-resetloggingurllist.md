---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.ResetLoggingUrlList
title: IWMReaderNetworkConfig::ResetLoggingUrlList
author: windows-sdk-content
description: The ResetLoggingUrlList method clears the list of servers that receive logging data.
old-location: wmformat\iwmreadernetworkconfig_resetloggingurllist.htm
old-project: wmformat
ms.assetid: 0fe71d73-a827-4aed-a37b-db7701cc1180
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],ResetLoggingUrlList method, IWMReaderNetworkConfig.ResetLoggingUrlList, IWMReaderNetworkConfig::ResetLoggingUrlList, IWMReaderNetworkConfigResetLoggingUrlList, ResetLoggingUrlList, ResetLoggingUrlList method [windows Media Format], ResetLoggingUrlList method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_resetloggingurllist, wmsdkidl/IWMReaderNetworkConfig::ResetLoggingUrlList
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
 - IWMReaderNetworkConfig.ResetLoggingUrlList
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::ResetLoggingUrlList


## -description



The <b>ResetLoggingUrlList</b> method clears the list of servers that receive logging data.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method removes any servers that were added using the <a href="https://msdn.microsoft.com/471b17c8-20e4-44f3-88ee-48a35cd8930c">IWMReaderNetworkConfig::AddLoggingUrl</a> method. Note that the originating server always receives a log, even after the list is cleared.




## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>
 

 

