---
UID: NF:wmsdkidl.IWMHeaderInfo.GetAttributeCount
title: IWMHeaderInfo::GetAttributeCount
author: windows-sdk-content
description: The GetAttributeCount method returns the number of attributes defined in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::GetAttributeCountEx and IWMHeaderInfo3::GetAttributeIndices, and should no longer be used.
old-location: wmformat\iwmheaderinfo_getattributecount.htm
tech.root: wmformat
ms.assetid: d5f0be62-4f15-45ca-8593-f5703a1f932a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAttributeCount, GetAttributeCount method [windows Media Format], GetAttributeCount method [windows Media Format],IWMHeaderInfo interface, GetAttributeCount method [windows Media Format],IWMHeaderInfo2 interface, GetAttributeCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo.GetAttributeCount, IWMHeaderInfo2 interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo2::GetAttributeCount, IWMHeaderInfo3 interface [windows Media Format],GetAttributeCount method, IWMHeaderInfo3::GetAttributeCount, IWMHeaderInfo::GetAttributeCount, IWMHeaderInfoGetAttributeCount, wmformat.iwmheaderinfo_getattributecount, wmsdkidl/IWMHeaderInfo2::GetAttributeCount, wmsdkidl/IWMHeaderInfo3::GetAttributeCount, wmsdkidl/IWMHeaderInfo::GetAttributeCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - qasf.dll
api_name:
 - IWMHeaderInfo.GetAttributeCount
 - IWMHeaderInfo2.GetAttributeCount
 - IWMHeaderInfo3.GetAttributeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMHeaderInfo::GetAttributeCount


## -description



The <b>GetAttributeCount</b> method returns the number of attributes defined in the header section of the ASF file. This method is replaced by <a href="https://msdn.microsoft.com/8c56d7b6-4f59-450e-938c-b7d0bd37ea08">IWMHeaderInfo3::GetAttributeCountEx</a> and <a href="https://msdn.microsoft.com/15c8f0c2-f2d4-441a-b6a9-774da820d03c">IWMHeaderInfo3::GetAttributeIndices</a>, and should no longer be used.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Pass zero for file-level attributes.


### -param pcAttributes [out]

Pointer to a count of the attributes.


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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state, or no profile has been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or <i>pcAttributes</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcAttributes</i> is not a valid pointer.

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



Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero.




## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/174969a2-4fe2-477b-9990-051d23bf8a29">IWMHeaderInfo::SetAttribute</a>
 

 

