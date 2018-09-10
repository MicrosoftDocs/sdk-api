---
UID: NF:wmsdkidl.IWMWriterFileSink3.GetMode
title: IWMWriterFileSink3::GetMode
author: windows-sdk-content
description: The GetMode method retrieves the supported file sink mode. More than one mode can be supported.
old-location: wmformat\iwmwriterfilesink3_getmode.htm
tech.root: wmformat
ms.assetid: a8a7003e-e59f-451c-9f45-75d6d094a03b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMode, GetMode method [windows Media Format], GetMode method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],GetMode method, IWMWriterFileSink3.GetMode, IWMWriterFileSink3::GetMode, IWMWriterFileSink3GetMode, wmformat.iwmwriterfilesink3_getmode, wmsdkidl/IWMWriterFileSink3::GetMode
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
 - IWMWriterFileSink3.GetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink3::GetMode


## -description



The <b>GetMode</b> method retrieves the supported file sink mode. More than one mode can be supported.




## -parameters




### -param pdwFileSinkMode [out]

Pointer to a <b>DWORD</b> containing a value from the <a href="https://msdn.microsoft.com/27846996-1957-4b19-91da-feeef477b06a">WMT_FILESINK_MODE</a> enumeration type or multiple values combined with a bitwise <b>OR</b> operator.


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
<i>pdwFileSinkMode</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>
 

 

