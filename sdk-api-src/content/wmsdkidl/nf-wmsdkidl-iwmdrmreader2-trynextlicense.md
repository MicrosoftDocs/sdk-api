---
UID: NF:wmsdkidl.IWMDRMReader2.TryNextLicense
title: IWMDRMReader2::TryNextLicense (wmsdkidl.h)
description: The TryNextLicense method sets the reader to evaluate the next applicable license (if present) for the file loaded in the reader.helpviewer_keywords: ["IWMDRMReader2 interface [windows Media Format]","TryNextLicense method","IWMDRMReader2.TryNextLicense","IWMDRMReader2::TryNextLicense","IWMDRMReader2TryNextLicense","TryNextLicense","TryNextLicense method [windows Media Format]","TryNextLicense method [windows Media Format]","IWMDRMReader2 interface","wmformat.iwmdrmreader2_trynextlicense","wmsdkidl/IWMDRMReader2::TryNextLicense"]
old-location: wmformat\iwmdrmreader2_trynextlicense.htm
tech.root: wmformat
ms.assetid: 2658abd7-61ca-452f-92ad-93ee5050603d
ms.date: 12/05/2018
ms.keywords: IWMDRMReader2 interface [windows Media Format],TryNextLicense method, IWMDRMReader2.TryNextLicense, IWMDRMReader2::TryNextLicense, IWMDRMReader2TryNextLicense, TryNextLicense, TryNextLicense method [windows Media Format], TryNextLicense method [windows Media Format],IWMDRMReader2 interface, wmformat.iwmdrmreader2_trynextlicense, wmsdkidl/IWMDRMReader2::TryNextLicense
f1_keywords:
- wmsdkidl/IWMDRMReader2.TryNextLicense
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMDRMReader2.TryNextLicense
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMReader2::TryNextLicense


## -description


<p class="CCE_Message">[<b>TryNextLicense</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>TryNextLicense</b> method sets the reader to evaluate the next applicable license (if present) for the file loaded in the reader.




## -parameters






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
<dt><b>DRM_S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more licenses for this content.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
No file is opened in the reader.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_RIV_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
An updated content revocation list is needed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The file opened in the reader is not protected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2">IWMDRMReader2 Interface</a>
 

 

