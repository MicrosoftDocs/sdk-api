---
UID: NF:wmsdkidl.IWMWriter.GetInputFormatCount
title: IWMWriter::GetInputFormatCount (wmsdkidl.h)
author: windows-sdk-content
description: The GetInputFormatCount method retrieves the number of media format types supported by this input on the writer.
old-location: wmformat\iwmwriter_getinputformatcount.htm
tech.root: wmformat
ms.assetid: c3afe9e8-e045-4329-b3e5-6026147322ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputFormatCount, GetInputFormatCount method [windows Media Format], GetInputFormatCount method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputFormatCount method, IWMWriter.GetInputFormatCount, IWMWriter::GetInputFormatCount, IWMWriterGetInputFormatCount, wmformat.iwmwriter_getinputformatcount, wmsdkidl/IWMWriter::GetInputFormatCount
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
 - IWMWriter.GetInputFormatCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriter::GetInputFormatCount


## -description



The <b>GetInputFormatCount</b> method retrieves the number of media format types supported by this input on the writer.




## -parameters




### -param dwInputNumber [in]

<b>DWORD</b> containing the input number.


### -param pcFormats [out]

Pointer to a count of formats.


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
The <i>pcFormats</i> parameter is <b>NULL</b>.

OR

<i>dwInputNumber</i> is too large.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798719(v=VS.85).aspx">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757478(v=VS.85).aspx">IWMWriter::GetInputFormat</a>



<a href="https://msdn.microsoft.com/482adfc4-d9ed-403d-912b-1a5a70baf04c">To Enumerate Input Formats</a>
 

 

