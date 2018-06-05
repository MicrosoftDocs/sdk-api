---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetUDPPortRanges
title: IWMReaderNetworkConfig::GetUDPPortRanges
author: windows-sdk-content
description: The GetUDPPortRanges method retrieves the UDP port number ranges used for receiving data.
old-location: wmformat\iwmreadernetworkconfig_getudpportranges.htm
old-project: wmformat
ms.assetid: a1792fd0-e9c3-4e28-9928-a615e1c9aec8
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetUDPPortRanges, GetUDPPortRanges method [windows Media Format], GetUDPPortRanges method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetUDPPortRanges method, IWMReaderNetworkConfig.GetUDPPortRanges, IWMReaderNetworkConfig::GetUDPPortRanges, IWMReaderNetworkConfigGetUDPPortRanges, wmformat.iwmreadernetworkconfig_getudpportranges, wmsdkidl/IWMReaderNetworkConfig::GetUDPPortRanges
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
-	IWMReaderNetworkConfig.GetUDPPortRanges
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetUDPPortRanges


## -description



The <b>GetUDPPortRanges</b> method retrieves the UDP port number ranges used for receiving data.




## -parameters




### -param pRangeArray [out]

Pointer to an array of <a href="https://msdn.microsoft.com/122db3fa-36bb-4d0c-9d05-0b7ae37f9187">WM_PORT_NUMBER_RANGE</a> structures allocated by the caller. Pass <b>NULL</b> to get the size of the array.


### -param pcRanges [in, out]

On input, pointer to a <b>DWORD</b> containing the length of the array passed in <i>pRangeArray</i>. On output, pointer to the required array size.


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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcRanges</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to this method. On the first call, pass <b>NULL</b> for <i>pRangeArray</i>. On return, the value pointed to by <i>pcRanges</i> is set to the size of the array that you should allocate. Then you can allocate the required amount of memory for the array and pass a pointer to it as <i>pRangeArray</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/9a61943a-8ff9-4504-b76f-25e3c5c8d4a4">IWMReaderNetworkConfig::SetUDPPortRanges</a>
 

 

