---
UID: NF:wmsdkidl.IWMStreamConfig.SetStreamNumber
title: IWMStreamConfig::SetStreamNumber
author: windows-sdk-content
description: The SetStreamNumber method specifies the stream number.
old-location: wmformat\iwmstreamconfig_setstreamnumber.htm
old-project: wmformat
ms.assetid: aea8b219-5b47-4176-ad96-d52646d96578
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMStreamConfig interface [windows Media Format],SetStreamNumber method, IWMStreamConfig.SetStreamNumber, IWMStreamConfig::SetStreamNumber, IWMStreamConfigSetStreamNumber, SetStreamNumber, SetStreamNumber method [windows Media Format], SetStreamNumber method [windows Media Format],IWMStreamConfig interface, wmformat.iwmstreamconfig_setstreamnumber, wmsdkidl/IWMStreamConfig::SetStreamNumber
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
 - IWMStreamConfig.SetStreamNumber
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig::SetStreamNumber


## -description



The <b>SetStreamNumber</b> method specifies the stream number.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers must be in the range of 1 through 63.


## -returns



This method always returns S_OK.




## -remarks



The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/2996c897-eb38-4432-8bf7-549023ab00f5">IWMStreamConfig::GetStreamNumber</a>
 

 

