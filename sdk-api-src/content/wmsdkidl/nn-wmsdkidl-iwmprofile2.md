---
UID: NN:wmsdkidl.IWMProfile2
title: IWMProfile2 (wmsdkidl.h)
description: The IWMProfile2 interface exposes the globally unique identifier for a system profile.helpviewer_keywords: ["IWMProfile2","IWMProfile2 interface [windows Media Format]","IWMProfile2 interface [windows Media Format]","described","IWMProfile2Interface","wmformat.iwmprofile2","wmsdkidl/IWMProfile2"]
old-location: wmformat\iwmprofile2.htm
tech.root: wmformat
ms.assetid: 34e30edb-3247-4eaa-9a63-6d94c9e37c0b
ms.date: 12/05/2018
ms.keywords: IWMProfile2, IWMProfile2 interface [windows Media Format], IWMProfile2 interface [windows Media Format],described, IWMProfile2Interface, wmformat.iwmprofile2, wmsdkidl/IWMProfile2
f1_keywords:
- wmsdkidl/IWMProfile2
dev_langs:
- c++
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
- IWMProfile2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile2 interface


## -description



The <b>IWMProfile2</b> interface exposes the globally unique identifier for a system profile. System profiles have associated identifiers, but custom profiles do not.

As with <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a>, <b>IWMProfile2</b> is included in profile objects as well as in reader and synchronous reader objects. To obtain a pointer to an <b>IWMProfile2</b> interface, call the <b>QueryInterface</b> method of any interface in one of these objects. For more information, see <b>IWMProfile Interface</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile</a>. <b>IWMProfile2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfile2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile2-getprofileid">GetProfileID</a>
</td>
<td align="left" width="63%">
Retrieves the globally unique identifier of the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
 

 

