---
UID: NF:wmsdkidl.IWMSyncReader.SetOutputProps
title: IWMSyncReader::SetOutputProps
author: windows-sdk-content
description: The SetOutputProps method specifies the media properties of an uncompressed output stream.
old-location: wmformat\iwmsyncreader_setoutputprops.htm
old-project: wmformat
ms.assetid: 5575fd7c-5eb0-4e4a-957d-e3fc174316ff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMSyncReader interface [windows Media Format],SetOutputProps method, IWMSyncReader.SetOutputProps, IWMSyncReader::SetOutputProps, IWMSyncReaderSetOutputProps, SetOutputProps, SetOutputProps method [windows Media Format], SetOutputProps method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setoutputprops, wmsdkidl/IWMSyncReader::SetOutputProps
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMSyncReader.SetOutputProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::SetOutputProps


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
The <i>dwOutputNum</i> parameter is greater than or equal to the number of outputs. Output numbers begin with zero.

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

DirectX VA formats can be returned from <a href="https://msdn.microsoft.com/7faac9e7-ad5f-42a4-ba6e-562ae973f81b">GetOutputFormat</a>, but if they are passed in to <b>SetOutputProps</b>, that method will fail because DirectX VA formats cannot be specified in this way. Therefore, your code should either examine the format before passing it to <b>SetOutputProps</b>, or else handle the case of that method failing by attempting the next format enumerated from <b>GetOutputFormat</b>.. For example code showing how to identify a DirectX VA format, see <a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>.

You can call <b>SetOutputProps</b> at any time after a file has been loaded into the synchronous reader. You can continue making calls as needed during playback.

New output properties set with this method will take effect with the next call to <b>GetNextSample</b>.




## -see-also




<a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps Interface</a>



<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/a5e701ea-8b53-4abe-8b78-7c6fb151d80f">IWMSyncReader::GetOutputProps</a>
 

 

