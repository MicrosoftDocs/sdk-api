---
UID: NN:mbnapi.IMbnConnectionProfile
title: IMbnConnectionProfile (mbnapi.h)
author: windows-sdk-content
description: This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.
old-location: mbn\imbnconnectionprofile.htm
tech.root: mbn
ms.assetid: f7730efe-e367-4642-8482-2a23052bab0c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnConnectionProfile, IMbnConnectionProfile interface [Microsoft Broadband Networks], IMbnConnectionProfile interface [Microsoft Broadband Networks],described, mbn.imbnconnectionprofile, mbnapi/IMbnConnectionProfile
ms.topic: interface
f1_keywords: ["mbnapi/IMbnConnectionProfile"]
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnConnectionProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfile interface


## -description


This interface accesses connection parameters and preferences stored in Mobile Broadband profiles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnConnectionProfile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnectionProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnConnectionProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofile-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofile-getprofilexmldata">GetProfileXmlData</a>
</td>
<td align="left" width="63%">
Gets the XML data of the current profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofile-updateprofile">UpdateProfile</a>
</td>
<td align="left" width="63%">
Updates the contents of the profile.

</td>
</tr>
</table> 


## -remarks



<b>IMbnConnectionProfile</b> objects are provided by calls to the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofile">GetConnectionProfile</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofiles">GetConnectionProfiles</a> methods of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager">IMbnConnectionProfileManager</a> interface.



