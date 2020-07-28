---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableContentCaching
title: IWMReaderNetworkConfig2::GetEnableContentCaching (wmsdkidl.h)
description: The GetEnableContentCaching method queries whether content caching is enabled. If content caching is enabled, streaming content can be cached locally.
helpviewer_keywords: ["GetEnableContentCaching","GetEnableContentCaching method [windows Media Format]","GetEnableContentCaching method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetEnableContentCaching method","IWMReaderNetworkConfig2.GetEnableContentCaching","IWMReaderNetworkConfig2::GetEnableContentCaching","IWMReaderNetworkConfig2GetEnableContentCaching","wmformat.iwmreadernetworkconfig2_getenablecontentcaching","wmsdkidl/IWMReaderNetworkConfig2::GetEnableContentCaching"]
old-location: wmformat\iwmreadernetworkconfig2_getenablecontentcaching.htm
tech.root: wmformat
ms.assetid: c8fdbb18-ba50-47e7-b7c9-858e6c452071
ms.date: 12/05/2018
ms.keywords: GetEnableContentCaching, GetEnableContentCaching method [windows Media Format], GetEnableContentCaching method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetEnableContentCaching method, IWMReaderNetworkConfig2.GetEnableContentCaching, IWMReaderNetworkConfig2::GetEnableContentCaching, IWMReaderNetworkConfig2GetEnableContentCaching, wmformat.iwmreadernetworkconfig2_getenablecontentcaching, wmsdkidl/IWMReaderNetworkConfig2::GetEnableContentCaching
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig2.GetEnableContentCaching
dev_langs:
- c++
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
- IWMReaderNetworkConfig2.GetEnableContentCaching
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig2::GetEnableContentCaching


## -description



The <b>GetEnableContentCaching</b> method queries whether content caching is enabled. If content caching is enabled, streaming content can be cached locally.




## -parameters




### -param pfEnableContentCaching [out]

Pointer to a Boolean value that is True if content caching is enabled.


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
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method applies only to content being streamed from a server running Windows Media Services.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching">IWMReaderNetworkConfig2::SetEnableContentCaching</a>
 

 

