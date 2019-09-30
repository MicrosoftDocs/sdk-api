---
UID: NN:wmsdkidl.IWMCodecInfo2
title: IWMCodecInfo2 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMCodecInfo2 interface manages the retrieval of information about codecs. To access it, call QueryInterface on a profile manager object.
old-location: wmformat\iwmcodecinfo2.htm
tech.root: wmformat
ms.assetid: 0cfb355e-af68-400d-aa64-57f17e7d936b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMCodecInfo2, IWMCodecInfo2 interface [windows Media Format], IWMCodecInfo2 interface [windows Media Format],described, IWMCodecInfo2Interface, wmformat.iwmcodecinfo2, wmsdkidl/IWMCodecInfo2
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMCodecInfo2"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMCodecInfo2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecInfo2 interface


## -description



The <b>IWMCodecInfo2</b> interface manages the retrieval of information about codecs. To access it, call <b>QueryInterface</b> on a profile manager object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecInfo2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo</a>. <b>IWMCodecInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc">GetCodecFormatDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of a specified codec format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecname">GetCodecName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a specified codec.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3</a>
</td>
<td>IID_IWMCodecInfo3</td>
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



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
 

 

