---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetUDPPortRanges
title: IWMReaderNetworkConfig::SetUDPPortRanges method
author: windows-driver-content
description: The SetUDPPortRanges method specifies the UDP port number ranges that are used for receiving data.
old-location: wmformat\iwmreadernetworkconfig_setudpportranges.htm
old-project: wmformat
ms.assetid: 9a61943a-8ff9-4504-b76f-25e3c5c8d4a4
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMReaderNetworkConfig, IWMReaderNetworkConfig interface [windows Media Format], SetUDPPortRanges method, IWMReaderNetworkConfig::SetUDPPortRanges, IWMReaderNetworkConfigSetUDPPortRanges, SetUDPPortRanges method [windows Media Format], SetUDPPortRanges method [windows Media Format], IWMReaderNetworkConfig interface, SetUDPPortRanges,IWMReaderNetworkConfig.SetUDPPortRanges, wmformat.iwmreadernetworkconfig_setudpportranges, wmsdkidl/IWMReaderNetworkConfig::SetUDPPortRanges
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IWMReaderNetworkConfig.SetUDPPortRanges
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetUDPPortRanges method


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




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/a1792fd0-e9c3-4e28-9928-a615e1c9aec8">IWMReaderNetworkConfig::GetUDPPortRanges</a>



<a href="https://msdn.microsoft.com/122db3fa-36bb-4d0c-9d05-0b7ae37f9187">WM_PORT_NUMBER_RANGE</a>
 

 

