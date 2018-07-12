---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetEnableContentCaching
title: IWMReaderNetworkConfig2::SetEnableContentCaching
author: windows-sdk-content
description: The SetEnableContentCaching method enables or disables content caching. If content caching is enabled, content that is being streamed can be cached locally.
old-location: wmformat\iwmreadernetworkconfig2_setenablecontentcaching.htm
old-project: wmformat
ms.assetid: 68dcb12e-e254-407e-864b-54d4e84b08ed
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetEnableContentCaching method, IWMReaderNetworkConfig2.SetEnableContentCaching, IWMReaderNetworkConfig2::SetEnableContentCaching, IWMReaderNetworkConfig2SetEnableContentCaching, SetEnableContentCaching, SetEnableContentCaching method [windows Media Format], SetEnableContentCaching method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setenablecontentcaching, wmsdkidl/IWMReaderNetworkConfig2::SetEnableContentCaching
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig2.SetEnableContentCaching
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::SetEnableContentCaching


## -description



The <b>SetEnableContentCaching</b> method enables or disables content caching. If content caching is enabled, content that is being streamed can be cached locally.




## -parameters




### -param fEnableContentCaching [in]

Boolean value that is True to enable content caching.


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
</table>
 




## -remarks



This method applies only to content being streamed from a server running Windows Media Services.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/c8fdbb18-ba50-47e7-b7c9-858e6c452071">IWMReaderNetworkConfig2::GetEnableContentCaching</a>
 

 

