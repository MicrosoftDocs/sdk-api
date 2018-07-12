---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableFastCache
title: IWMReaderNetworkConfig2::GetEnableFastCache
author: windows-sdk-content
description: The GetEnableFastCache method queries whether Fast Cache streaming is enabled. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.
old-location: wmformat\iwmreadernetworkconfig2_getenablefastcache.htm
old-project: wmformat
ms.assetid: 50f904a3-5a2d-4c0f-92fe-76a1ff195c91
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetEnableFastCache, GetEnableFastCache method [windows Media Format], GetEnableFastCache method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetEnableFastCache method, IWMReaderNetworkConfig2.GetEnableFastCache, IWMReaderNetworkConfig2::GetEnableFastCache, IWMReaderNetworkConfig2GetEnableFastCache, wmformat.iwmreadernetworkconfig2_getenablefastcache, wmsdkidl/IWMReaderNetworkConfig2::GetEnableFastCache
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
 - IWMReaderNetworkConfig2.GetEnableFastCache
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::GetEnableFastCache


## -description



The <b>GetEnableFastCache</b> method queries whether Fast Cache streaming is enabled. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.




## -parameters




### -param pfEnableFastCache [out]

Pointer to a variable that receives a Boolean value. The value is True if Fast Cache streaming is enabled, or False otherwise.


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



This feature requires content caching to be enabled as well. Fast Cache applies only to content being streamed from a server running Windows Media Services.




## -see-also




<a href="https://msdn.microsoft.com/2a850d6f-8e1d-4aeb-9791-c51c3debf118">Enabling Fast Cache Streaming from the Client</a>



<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/28a01985-a133-4203-8385-d4497c29bf9c">IWMReaderNetworkConfig2::SetEnableFastCache</a>
 

 

