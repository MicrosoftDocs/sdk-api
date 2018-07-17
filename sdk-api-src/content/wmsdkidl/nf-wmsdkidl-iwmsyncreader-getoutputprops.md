---
UID: NF:wmsdkidl.IWMSyncReader.GetOutputProps
title: IWMSyncReader::GetOutputProps
author: windows-sdk-content
description: The GetOutputProps method retrieves the current properties of an uncompressed output stream.
old-location: wmformat\iwmsyncreader_getoutputprops.htm
old-project: wmformat
ms.assetid: a5e701ea-8b53-4abe-8b78-7c6fb151d80f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetOutputProps, GetOutputProps method [windows Media Format], GetOutputProps method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetOutputProps method, IWMSyncReader.GetOutputProps, IWMSyncReader::GetOutputProps, IWMSyncReaderGetOutputProps, wmformat.iwmsyncreader_getoutputprops, wmsdkidl/IWMSyncReader::GetOutputProps
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
 - IWMSyncReader.GetOutputProps
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSyncReader::GetOutputProps


## -description



The <b>GetOutputProps</b> method retrieves the current properties of an uncompressed output stream.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param ppOutput [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a> interface, which is created by a successful call to this method.


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
The <i>ppOutput</i> parameter is <b>NULL</b>, or the <i>dwOutputNum</i> parameter is greater than or equal to the number of outputs. Output numbers begin with zero.

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



Manipulating the object retrieved by a call to <b>GetOutputProps</b> has no effect on the output media stream, unless the application also calls <b>SetOutputProps</b>.




## -see-also




<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/5575fd7c-5eb0-4e4a-957d-e3fc174316ff">IWMSyncReader::SetOutputProps</a>
 

 

