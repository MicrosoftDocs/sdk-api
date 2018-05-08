---
UID: NF:wmsdkidl.IWMStreamConfig.GetStreamType
title: IWMStreamConfig::GetStreamType
author: windows-driver-content
description: The GetStreamType method retrieves the major type of the stream (audio, video, or script).
old-location: wmformat\iwmstreamconfig_getstreamtype.htm
old-project: wmformat
ms.assetid: a8dc8c37-da52-4d0f-b143-aaa45e6f77b8
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetStreamType, GetStreamType method [windows Media Format], GetStreamType method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetStreamType method, IWMStreamConfig.GetStreamType, IWMStreamConfig::GetStreamType, IWMStreamConfigGetStreamType, wmformat.iwmstreamconfig_getstreamtype, wmsdkidl/IWMStreamConfig::GetStreamType
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
-	IWMStreamConfig.GetStreamType
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig::GetStreamType


## -description



The <b>GetStreamType</b> method retrieves the major type of the stream (audio, video, or script).




## -parameters




### -param pguidStreamType [out]

Pointer to a GUID object specifying the major type of the stream.


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
The <i>pguidStreamType</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GUID_NULL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMediaType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For a table of stream major types, see <a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/86c65cfe-d482-461b-a187-ce1ce9a30609">IWMStreamConfig::GetStreamName</a>
 

 

