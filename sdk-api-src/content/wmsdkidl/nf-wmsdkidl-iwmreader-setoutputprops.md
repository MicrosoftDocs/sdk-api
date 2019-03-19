---
UID: NF:wmsdkidl.IWMReader.SetOutputProps
title: IWMReader::SetOutputProps (wmsdkidl.h)
author: windows-sdk-content
description: The SetOutputProps method specifies the media properties of an uncompressed output stream.
old-location: wmformat\iwmreader_setoutputprops.htm
tech.root: wmformat
ms.assetid: 0a5325d1-880b-4d65-96af-9d311dca989b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReader interface [windows Media Format],SetOutputProps method, IWMReader.SetOutputProps, IWMReader::SetOutputProps, IWMReaderSetOutputProps, SetOutputProps, SetOutputProps method [windows Media Format], SetOutputProps method [windows Media Format],IWMReader interface, wmformat.iwmreader_setoutputprops, wmsdkidl/IWMReader::SetOutputProps
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
 - IWMReader.SetOutputProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReader::SetOutputProps


## -description



The <b>SetOutputProps</b> method specifies the media properties of an uncompressed output stream.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pOutput [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dd757252(v=VS.85).aspx">IWMOutputMediaProps</a> interface.


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
The <i>dwOutputNum</i> parameter is greater than the number of output streams.

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



Manipulating an object retrieved by a call to <b>GetOutputProps</b> has no effect on the output media stream unless the application also calls <b>SetOutputProps</b>.

DirectX VA formats can be returned from <a href="https://msdn.microsoft.com/en-us/library/Dd798589(v=VS.85).aspx">GetOutputFormat</a>, but if they are passed in to <b>SetOutputProps</b>, that method will fail because DirectX VA formats cannot be specified in this way. Therefore, your code should either examine the format before passing it to <b>SetOutputProps</b>, or handle the case of that method failing by attempting the next format enumerated from <b>GetOutputFormat</b>. For a code snippet showing how to identify a DirectX VA format, see <a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>


If this method is called while the reader is running, an <a href="https://msdn.microsoft.com/en-us/library/Dd743497(v=VS.85).aspx">IWMReaderCallbackAdvanced::OnOutputPropsChanged</a> call is generated.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757425(v=VS.85).aspx">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743595(v=VS.85).aspx">IWMReader::GetOutputProps</a>
 

 

