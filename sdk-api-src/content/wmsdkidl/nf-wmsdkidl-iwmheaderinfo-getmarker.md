---
UID: NF:wmsdkidl.IWMHeaderInfo.GetMarker
title: IWMHeaderInfo::GetMarker
author: windows-sdk-content
description: The GetMarker method returns the name and time of a marker.
old-location: wmformat\iwmheaderinfo_getmarker.htm
old-project: wmformat
ms.assetid: ae035991-86c8-4ffc-b819-5a5ce81a980f
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetMarker, GetMarker method [windows Media Format], GetMarker method [windows Media Format],IWMHeaderInfo interface, GetMarker method [windows Media Format],IWMHeaderInfo2 interface, GetMarker method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetMarker method, IWMHeaderInfo.GetMarker, IWMHeaderInfo2 interface [windows Media Format],GetMarker method, IWMHeaderInfo2::GetMarker, IWMHeaderInfo3 interface [windows Media Format],GetMarker method, IWMHeaderInfo3::GetMarker, IWMHeaderInfo::GetMarker, IWMHeaderInfoGetMarker, wmformat.iwmheaderinfo_getmarker, wmsdkidl/IWMHeaderInfo2::GetMarker, wmsdkidl/IWMHeaderInfo3::GetMarker, wmsdkidl/IWMHeaderInfo::GetMarker
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
 - IWMHeaderInfo.GetMarker
 - IWMHeaderInfo2.GetMarker
 - IWMHeaderInfo3.GetMarker
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::GetMarker


## -description



The <b>GetMarker</b> method returns the name and time of a <a href="wmformat_glossary.htm">marker</a>.




## -parameters




### -param wIndex [in]

<b>WORD</b> containing the index.


### -param pwszMarkerName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the marker name.


### -param pcchMarkerNameLen [in]

On input, a pointer to a variable containing the length of the <i>pwszMarkerName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the name, including the terminating <b>null</b> character. To retrieve the length of the name, you must set this to zero and set <i>pwszMarkerName</i> and <i>pcnsMarkerTime</i> to <b>NULL</b>.


### -param pcnsMarkerTime [out]

Pointer to a variable specifying the marker time in 100-nanosecond increments.


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
The size specified by <i>pcchMarkerNameLen</i> is too small to receive the name.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcchMarkerNameLen</i> is <b>NULL</b>, or another parameter does not contain a valid value.

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
 




## -remarks



The writer does not support markers, and returns E_NOTIMPL when this method is called.




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/cfa111bb-7bbb-448a-b2db-d36637c01a52">IWMHeaderInfo::AddMarker</a>



<a href="https://msdn.microsoft.com/c0d8e61d-8703-407a-9610-9e9f29ab92a1">IWMHeaderInfo::GetMarkerCount</a>



<a href="https://msdn.microsoft.com/b95aa113-b218-44ef-9516-20894e02ee6c">IWMHeaderInfo::RemoveMarker</a>



<a href="https://msdn.microsoft.com/ba9bc93e-76a9-4a49-951f-c38dbcceef8c">Markers</a>
 

 

