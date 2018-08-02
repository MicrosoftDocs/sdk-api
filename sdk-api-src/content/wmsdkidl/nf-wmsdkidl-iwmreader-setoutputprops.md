---
UID: NF:wmsdkidl.IWMReader.SetOutputProps
title: IWMReader::SetOutputProps
author: windows-sdk-content
description: The SetOutputProps method specifies the media properties of an uncompressed output stream.
old-location: wmformat\iwmreader_setoutputprops.htm
old-project: wmformat
ms.assetid: 0a5325d1-880b-4d65-96af-9d311dca989b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMReader interface [windows Media Format],SetOutputProps method, IWMReader.SetOutputProps, IWMReader::SetOutputProps, IWMReaderSetOutputProps, SetOutputProps, SetOutputProps method [windows Media Format], SetOutputProps method [windows Media Format],IWMReader interface, wmformat.iwmreader_setoutputprops, wmsdkidl/IWMReader::SetOutputProps
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
api_name:
 - IWMReader.SetOutputProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReader::SetOutputProps


## -description



The <b>SetOutputProps</b> method specifies the media properties of an uncompressed output stream.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pOutput [in]

Pointer to an <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a> interface.


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

DirectX VA formats can be returned from <a href="https://msdn.microsoft.com/7faac9e7-ad5f-42a4-ba6e-562ae973f81b">GetOutputFormat</a>, but if they are passed in to <b>SetOutputProps</b>, that method will fail because DirectX VA formats cannot be specified in this way. Therefore, your code should either examine the format before passing it to <b>SetOutputProps</b>, or handle the case of that method failing by attempting the next format enumerated from <b>GetOutputFormat</b>. For a code snippet showing how to identify a DirectX VA format, see <a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>


If this method is called while the reader is running, an <a href="https://msdn.microsoft.com/5e8193c4-5fc7-4b19-9f6e-6873ebe5156a">IWMReaderCallbackAdvanced::OnOutputPropsChanged</a> call is generated.




## -see-also




<a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader Interface</a>



<a href="https://msdn.microsoft.com/8958abd0-cc2b-4d02-a831-c998d468fb06">IWMReader::GetOutputProps</a>
 

 

