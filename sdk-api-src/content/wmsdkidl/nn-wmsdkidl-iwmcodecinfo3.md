---
UID: NN:wmsdkidl.IWMCodecInfo3
title: IWMCodecInfo3 (wmsdkidl.h)
description: The IWMCodecInfo3 interface retrieves properties from a codec.You can retrieve a pointer to IWMCodecInfo3 with a call to the QueryInterface method of any other interface of the profile manager object.
helpviewer_keywords: ["IWMCodecInfo3","IWMCodecInfo3 interface [windows Media Format]","IWMCodecInfo3 interface [windows Media Format]","described","IWMCodecInfo3Interface","wmformat.iwmcodecinfo3","wmsdkidl/IWMCodecInfo3"]
old-location: wmformat\iwmcodecinfo3.htm
tech.root: wmformat
ms.assetid: fd882612-1f60-4b51-a180-0d34d78c99dd
ms.date: 12/05/2018
ms.keywords: IWMCodecInfo3, IWMCodecInfo3 interface [windows Media Format], IWMCodecInfo3 interface [windows Media Format],described, IWMCodecInfo3Interface, wmformat.iwmcodecinfo3, wmsdkidl/IWMCodecInfo3
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCodecInfo3
 - wmsdkidl/IWMCodecInfo3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMCodecInfo3
---

# IWMCodecInfo3 interface


## -description

The <b>IWMCodecInfo3</b> interface retrieves properties from a codec.

You can retrieve a pointer to <b>IWMCodecInfo3</b> with a call to the <b>QueryInterface</b> method of any other interface of the profile manager object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2</a>. <b>IWMCodecInfo3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecInfo3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecenumerationsetting">GetCodecEnumerationSetting</a>
</td>
<td align="left" width="63%">
Obtains the current value for a codec enumeration setting. Codec enumeration settings enable you to enumerate codec formats by feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecformatprop">GetCodecFormatProp</a>
</td>
<td align="left" width="63%">
Retrieves a property from one format of a codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop">GetCodecProp</a>
</td>
<td align="left" width="63%">
Retrieves a codec property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting">SetCodecEnumerationSetting</a>
</td>
<td align="left" width="63%">
Sets a codec enumeration setting. Codec enumeration settings enable you to enumerate codec formats by feature.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize</a>
</td>
<td>IID_IWMPacketSize</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2">IWMPacketSize2</a>
</td>
<td>IID_IWMPacketSize2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2">IWMProfileManager2</a>
</td>
<td>IID_IWMProfileManager2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>

