---
UID: NF:wmsdkidl.IWMWriter.GetInputCount
title: IWMWriter::GetInputCount (wmsdkidl.h)
author: windows-sdk-content
description: The GetInputCount method retrieves the number of uncompressed input streams.
old-location: wmformat\iwmwriter_getinputcount.htm
tech.root: wmformat
ms.assetid: 0cb3cd79-0640-4a3b-8e8b-d81df2ff749f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputCount, GetInputCount method [windows Media Format], GetInputCount method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],GetInputCount method, IWMWriter.GetInputCount, IWMWriter::GetInputCount, IWMWriterGetInputCount, wmformat.iwmwriter_getinputcount, wmsdkidl/IWMWriter::GetInputCount
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
 - IWMWriter.GetInputCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriter::GetInputCount


## -description



The <b>GetInputCount</b> method retrieves the number of uncompressed input streams.




## -parameters




### -param pcInputs [out]

Pointer to a count of inputs.


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
The <i>pcInputs</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method along with <a href="https://msdn.microsoft.com/en-us/library/Dd757482(v=VS.85).aspx">GetInputProps</a> can be used to enumerate through the various inputs, and get the input format of each. These are not the output Windows Media streams specified in the profile; in a multiple bit rate scenario, one input stream can map to multiple Windows Media streams.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798719(v=VS.85).aspx">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/f468f74d-7eed-4819-957d-241903f44d2d">To Identify Inputs By Number</a>
 

 

