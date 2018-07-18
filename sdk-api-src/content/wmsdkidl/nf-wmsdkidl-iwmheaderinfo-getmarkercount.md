---
UID: NF:wmsdkidl.IWMHeaderInfo.GetMarkerCount
title: IWMHeaderInfo::GetMarkerCount
author: windows-sdk-content
description: The GetMarkerCount method returns the number of markers currently in the header section of the ASF file.
old-location: wmformat\iwmheaderinfo_getmarkercount.htm
old-project: wmformat
ms.assetid: c0d8e61d-8703-407a-9610-9e9f29ab92a1
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetMarkerCount, GetMarkerCount method [windows Media Format], GetMarkerCount method [windows Media Format],IWMHeaderInfo interface, GetMarkerCount method [windows Media Format],IWMHeaderInfo2 interface, GetMarkerCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo.GetMarkerCount, IWMHeaderInfo2 interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo2::GetMarkerCount, IWMHeaderInfo3 interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo3::GetMarkerCount, IWMHeaderInfo::GetMarkerCount, IWMHeaderInfoGetMarkerCount, wmformat.iwmheaderinfo_getmarkercount, wmsdkidl/IWMHeaderInfo2::GetMarkerCount, wmsdkidl/IWMHeaderInfo3::GetMarkerCount, wmsdkidl/IWMHeaderInfo::GetMarkerCount
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
 - qasf.dll
api_name:
 - IWMHeaderInfo.GetMarkerCount
 - IWMHeaderInfo2.GetMarkerCount
 - IWMHeaderInfo3.GetMarkerCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::GetMarkerCount


## -description



The <b>GetMarkerCount</b> method returns the number of <a href="wmformat_glossary.htm">markers</a> currently in the header section of the ASF file.




## -parameters




### -param pcMarkers [out]

Pointer to a count of markers.


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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/ae035991-86c8-4ffc-b819-5a5ce81a980f">IWMHeaderInfo::GetMarker</a>



<a href="https://msdn.microsoft.com/ba9bc93e-76a9-4a49-951f-c38dbcceef8c">Markers</a>
 

 

