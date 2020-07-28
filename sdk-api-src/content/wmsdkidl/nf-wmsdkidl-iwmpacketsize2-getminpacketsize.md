---
UID: NF:wmsdkidl.IWMPacketSize2.GetMinPacketSize
title: IWMPacketSize2::GetMinPacketSize (wmsdkidl.h)
description: The GetMinPacketSize method retrieves the minimum packet size for files created with the profile. If you use this method from an interface belonging to a reader or synchronous reader object, the retrieved minimum packet size will always be zero.
helpviewer_keywords: ["GetMinPacketSize","GetMinPacketSize method [windows Media Format]","GetMinPacketSize method [windows Media Format]","IWMPacketSize2 interface","IWMPacketSize2 interface [windows Media Format]","GetMinPacketSize method","IWMPacketSize2.GetMinPacketSize","IWMPacketSize2::GetMinPacketSize","IWMPacketSize2GetMinPacketSize","wmformat.iwmpacketsize2_getminpacketsize","wmsdkidl/IWMPacketSize2::GetMinPacketSize"]
old-location: wmformat\iwmpacketsize2_getminpacketsize.htm
tech.root: wmformat
ms.assetid: 2b15f5b9-b7c1-4427-81d9-bbcd0bb0ce45
ms.date: 12/05/2018
ms.keywords: GetMinPacketSize, GetMinPacketSize method [windows Media Format], GetMinPacketSize method [windows Media Format],IWMPacketSize2 interface, IWMPacketSize2 interface [windows Media Format],GetMinPacketSize method, IWMPacketSize2.GetMinPacketSize, IWMPacketSize2::GetMinPacketSize, IWMPacketSize2GetMinPacketSize, wmformat.iwmpacketsize2_getminpacketsize, wmsdkidl/IWMPacketSize2::GetMinPacketSize
f1_keywords:
- wmsdkidl/IWMPacketSize2.GetMinPacketSize
dev_langs:
- c++
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
- IWMPacketSize2.GetMinPacketSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPacketSize2::GetMinPacketSize


## -description



The <b>GetMinPacketSize</b> method retrieves the minimum <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">packet</a> size for files created with the profile. If you use this method from an interface belonging to a reader or synchronous reader object, the retrieved minimum packet size will always be zero.




## -parameters




### -param pdwMinPacketSize [out]

Pointer to a <b>DWORD</b> that will receive the minimum packet size.


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
NULL pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2">IWMPacketSize2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize2-setminpacketsize">IWMPacketSize2::SetMinPacketSize</a>
 

 

