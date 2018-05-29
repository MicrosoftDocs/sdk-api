---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetEnableFastCache
title: IWMReaderNetworkConfig2::SetEnableFastCache
author: windows-sdk-content
description: The SetEnableFastCache method enables or disables Fast Cache streaming. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.
old-location: wmformat\iwmreadernetworkconfig2_setenablefastcache.htm
old-project: wmformat
ms.assetid: 28a01985-a133-4203-8385-d4497c29bf9c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetEnableFastCache method, IWMReaderNetworkConfig2.SetEnableFastCache, IWMReaderNetworkConfig2::SetEnableFastCache, IWMReaderNetworkConfig2SetEnableFastCache, SetEnableFastCache, SetEnableFastCache method [windows Media Format], SetEnableFastCache method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setenablefastcache, wmsdkidl/IWMReaderNetworkConfig2::SetEnableFastCache
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
-	IWMReaderNetworkConfig2.SetEnableFastCache
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::SetEnableFastCache


## -description



The <b>SetEnableFastCache</b> method enables or disables Fast Cache streaming. Fast Cache streaming enables network content to be streamed faster than the playback rate, if bandwidth allows.




## -parameters




### -param fEnableFastCache [in]

Specifies whether to enable or disable Fast Cache streaming. The value True enables Fast Cache, and the value False disables it.


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



This method enables the reader to use Fast Cache streaming if the server also supports it. This feature is supported only when streaming content from a server running Windows Media Services. For more information, see <a href="https://msdn.microsoft.com/2a850d6f-8e1d-4aeb-9791-c51c3debf118">Enabling Fast Cache Streaming from the Client</a>.

Regardless of the status of Fast Cache set by this method, a user can enable this feature by adding "?WMCache=1" to the end of the URL. However, Fast Cache cannot be activated at all unless caching is enabled with a call to <a href="https://msdn.microsoft.com/68dcb12e-e254-407e-864b-54d4e84b08ed">IWMReaderNetworkconfig2::SetEnableContentCaching</a>.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/50f904a3-5a2d-4c0f-92fe-76a1ff195c91">IWMReaderNetworkConfig2::GetEnableFastCache</a>
 

 

