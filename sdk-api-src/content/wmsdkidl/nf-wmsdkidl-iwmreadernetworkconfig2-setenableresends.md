---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetEnableResends
title: IWMReaderNetworkConfig2::SetEnableResends
author: windows-driver-content
description: The SetEnableResends method enables or disables resends.
old-location: wmformat\iwmreadernetworkconfig2_setenableresends.htm
old-project: wmformat
ms.assetid: c3bd0e03-eee1-4022-8540-1dcc927d6b5f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetEnableResends method, IWMReaderNetworkConfig2.SetEnableResends, IWMReaderNetworkConfig2::SetEnableResends, IWMReaderNetworkConfig2SetEnableResends, SetEnableResends, SetEnableResends method [windows Media Format], SetEnableResends method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setenableresends, wmsdkidl/IWMReaderNetworkConfig2::SetEnableResends
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWMReaderNetworkConfig2.SetEnableResends
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::SetEnableResends


## -description



The <b>SetEnableResends</b> method enables or disables resends.




## -parameters




### -param fEnableResends [in]

Pointer to a Boolean value that is True to enable resends.


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



This feature is available only for content streamed from a server running Windows Media Services using either MMSU or RTSPU protocol.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/d39d42c3-7d00-4fb6-8979-2b65d00ac636">IWMReaderNetworkConfig2::GetEnableResends</a>
 

 

