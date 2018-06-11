---
UID: NF:wmsdkidl.IWMHeaderInfo.RemoveMarker
title: IWMHeaderInfo::RemoveMarker
author: windows-sdk-content
description: The RemoveMarker method removes a marker from the header section of the ASF file.
old-location: wmformat\iwmheaderinfo_removemarker.htm
old-project: wmformat
ms.assetid: b95aa113-b218-44ef-9516-20894e02ee6c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMHeaderInfo interface [windows Media Format],RemoveMarker method, IWMHeaderInfo.RemoveMarker, IWMHeaderInfo2 interface [windows Media Format],RemoveMarker method, IWMHeaderInfo2::RemoveMarker, IWMHeaderInfo3 interface [windows Media Format],RemoveMarker method, IWMHeaderInfo3::RemoveMarker, IWMHeaderInfo::RemoveMarker, IWMHeaderInfoRemoveMarker, RemoveMarker, RemoveMarker method [windows Media Format], RemoveMarker method [windows Media Format],IWMHeaderInfo interface, RemoveMarker method [windows Media Format],IWMHeaderInfo2 interface, RemoveMarker method [windows Media Format],IWMHeaderInfo3 interface, wmformat.iwmheaderinfo_removemarker, wmsdkidl/IWMHeaderInfo2::RemoveMarker, wmsdkidl/IWMHeaderInfo3::RemoveMarker, wmsdkidl/IWMHeaderInfo::RemoveMarker
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
 - IWMHeaderInfo.RemoveMarker
 - IWMHeaderInfo2.RemoveMarker
 - IWMHeaderInfo3.RemoveMarker
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMHeaderInfo::RemoveMarker


## -description



The <b>RemoveMarker</b> method removes a <a href="wmformat_glossary.htm">marker</a> from the header section of the ASF file.




## -parameters




### -param wIndex [in]

<b>WORD</b> containing the index of the marker.


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
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no marker at <i>wIndex</i>.

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
 




## -remarks



This method is not supported by the writer.




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/cfa111bb-7bbb-448a-b2db-d36637c01a52">IWMHeaderInfo::AddMarker</a>



<a href="https://msdn.microsoft.com/ae035991-86c8-4ffc-b819-5a5ce81a980f">IWMHeaderInfo::GetMarker</a>



<a href="https://msdn.microsoft.com/ba9bc93e-76a9-4a49-951f-c38dbcceef8c">Markers</a>
 

 

