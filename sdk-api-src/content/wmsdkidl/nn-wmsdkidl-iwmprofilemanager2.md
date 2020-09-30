---
UID: NN:wmsdkidl.IWMProfileManager2
title: IWMProfileManager2 (wmsdkidl.h)
description: The IWMProfileManager2 interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager.
helpviewer_keywords: ["IWMProfileManager2","IWMProfileManager2 interface [windows Media Format]","IWMProfileManager2 interface [windows Media Format]","described","IWMProfileManager2Interface","wmformat.iwmprofilemanager2","wmsdkidl/IWMProfileManager2"]
old-location: wmformat\iwmprofilemanager2.htm
tech.root: wmformat
ms.assetid: eb5d904e-15ee-4066-ab05-c4e133bc89d7
ms.date: 12/05/2018
ms.keywords: IWMProfileManager2, IWMProfileManager2 interface [windows Media Format], IWMProfileManager2 interface [windows Media Format],described, IWMProfileManager2Interface, wmformat.iwmprofilemanager2, wmsdkidl/IWMProfileManager2
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
 - IWMProfileManager2
 - wmsdkidl/IWMProfileManager2
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
 - IWMProfileManager2
---

# IWMProfileManager2 interface


## -description

The <b>IWMProfileManager2</b> interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager. Most applications should set the value to the latest version unless they need to be backward-compatible with another application that was written using an earlier version of this SDK.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfileManager2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager</a>. <b>IWMProfileManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfileManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager2-getsystemprofileversion">GetSystemProfileVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the system profiles that the profile manager enumerates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager2-setsystemprofileversion">SetSystemProfileVersion</a>
</td>
<td align="left" width="63%">
Specifies the version number of the system profiles that the profile manager enumerates.

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
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo</a>
</td>
<td>IID_IWMCodecInfo</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2</a>
</td>
<td>IID_IWMCodecInfo2</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3</a>
</td>
<td>IID_IWMCodecInfo3</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager</a>
</td>
<td>IID_IWMProfileManager</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage">IWMProfileManagerLanguage</a>
</td>
<td>IID_IWMProfileManagerLanguage</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>