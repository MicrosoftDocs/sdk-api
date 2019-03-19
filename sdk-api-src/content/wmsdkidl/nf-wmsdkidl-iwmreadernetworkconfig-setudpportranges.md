---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetUDPPortRanges
title: IWMReaderNetworkConfig::SetUDPPortRanges (wmsdkidl.h)
author: windows-sdk-content
description: The SetUDPPortRanges method specifies the UDP port number ranges that are used for receiving data.
old-location: wmformat\iwmreadernetworkconfig_setudpportranges.htm
tech.root: wmformat
ms.assetid: 9a61943a-8ff9-4504-b76f-25e3c5c8d4a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetUDPPortRanges method, IWMReaderNetworkConfig.SetUDPPortRanges, IWMReaderNetworkConfig::SetUDPPortRanges, IWMReaderNetworkConfigSetUDPPortRanges, SetUDPPortRanges, SetUDPPortRanges method [windows Media Format], SetUDPPortRanges method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setudpportranges, wmsdkidl/IWMReaderNetworkConfig::SetUDPPortRanges
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
 - IWMReaderNetworkConfig.SetUDPPortRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::SetUDPPortRanges


## -description



The <b>SetUDPPortRanges</b> method specifies the UDP port number ranges that are used for receiving data.




## -parameters




### -param pRangeArray [in]

Pointer to an array of <b>WM_PORT_NUMBER_RANGE</b> structures.


### -param cRanges [in]

A value indicating the length of the array passed in <i>pRangeArray</i>.


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



If no ranges are specified by the application, port numbers are selected by the reader.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743504(v=VS.85).aspx">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743536(v=VS.85).aspx">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757979(v=VS.85).aspx">WM_PORT_NUMBER_RANGE</a>
 

 

