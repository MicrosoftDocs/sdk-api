---
UID: NF:wmsdkidl.IWMStreamConfig.GetBitrate
title: IWMStreamConfig::GetBitrate
author: windows-sdk-content
description: The GetBitrate method retrieves the bit rate for the stream.
old-location: wmformat\iwmstreamconfig_getbitrate.htm
tech.root: wmformat
ms.assetid: d34bea45-758e-4c4a-928f-229ce6b4241c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetBitrate, GetBitrate method [windows Media Format], GetBitrate method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetBitrate method, IWMStreamConfig.GetBitrate, IWMStreamConfig::GetBitrate, IWMStreamConfigGetBitrate, wmformat.iwmstreamconfig_getbitrate, wmsdkidl/IWMStreamConfig::GetBitrate
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
 - IWMStreamConfig.GetBitrate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamConfig::GetBitrate


## -description



The <b>GetBitrate</b> method retrieves the bit rate for the stream.




## -parameters




### -param pdwBitrate [out]

Pointer to a <b>DWORD</b> containing the bit rate, in bits per second.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwbitrate</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/202be688-e739-4e80-9574-f85b2eb168fc">IWMStreamConfig::SetBitrate</a>
 

 

