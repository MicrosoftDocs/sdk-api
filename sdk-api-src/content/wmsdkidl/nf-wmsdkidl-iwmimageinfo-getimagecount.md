---
UID: NF:wmsdkidl.IWMImageInfo.GetImageCount
title: IWMImageInfo::GetImageCount (wmsdkidl.h)
description: The GetImageCount method retrieves the number of images stored in a file using ID3v2 &#0034;APIC&#0034; frames. Images stored in the file using attributes in the Windows Media namespace, or any images stored in custom attributes, are not included in this count.
helpviewer_keywords: ["GetImageCount","GetImageCount method [windows Media Format]","GetImageCount method [windows Media Format]","IWMImageInfo interface","IWMImageInfo interface [windows Media Format]","GetImageCount method","IWMImageInfo.GetImageCount","IWMImageInfo::GetImageCount","IWMImageInfoGetImageCount","wmformat.iwmimageinfo_getimagecount","wmsdkidl/IWMImageInfo::GetImageCount"]
old-location: wmformat\iwmimageinfo_getimagecount.htm
tech.root: wmformat
ms.assetid: 95cf5906-9cbc-4bba-8892-236672cf4068
ms.date: 12/05/2018
ms.keywords: GetImageCount, GetImageCount method [windows Media Format], GetImageCount method [windows Media Format],IWMImageInfo interface, IWMImageInfo interface [windows Media Format],GetImageCount method, IWMImageInfo.GetImageCount, IWMImageInfo::GetImageCount, IWMImageInfoGetImageCount, wmformat.iwmimageinfo_getimagecount, wmsdkidl/IWMImageInfo::GetImageCount
f1_keywords:
- wmsdkidl/IWMImageInfo.GetImageCount
dev_langs:
- c++
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
- IWMImageInfo.GetImageCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMImageInfo::GetImageCount


## -description



The <b>GetImageCount</b> method retrieves the number of images stored in a file using ID3v2 "APIC" frames. Images stored in the file using attributes in the Windows Media namespace, or any images stored in custom attributes, are not included in this count.




## -parameters




### -param pcImages [out]

Pointer to the number of images.


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
The <i>pcImages</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
One of the ID3 frames that should be in the file cannot be accessed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo">IWMImageInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmimageinfo-getimage">IWMImageInfo::GetImage</a>
 

 

