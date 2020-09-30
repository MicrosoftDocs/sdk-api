---
UID: NN:mfidl.IMFNetCredential
title: IMFNetCredential (mfidl.h)
description: Sets and retrieves user-name and password information for authentication purposes.
helpviewer_keywords: ["IMFNetCredential","IMFNetCredential interface [Media Foundation]","IMFNetCredential interface [Media Foundation]","described","d202e7bc-9ce0-4861-8552-5a4d599b1661","mf.imfnetcredential","mfidl/IMFNetCredential"]
old-location: mf\imfnetcredential.htm
tech.root: mf
ms.assetid: d202e7bc-9ce0-4861-8552-5a4d599b1661
ms.date: 12/05/2018
ms.keywords: IMFNetCredential, IMFNetCredential interface [Media Foundation], IMFNetCredential interface [Media Foundation],described, d202e7bc-9ce0-4861-8552-5a4d599b1661, mf.imfnetcredential, mfidl/IMFNetCredential
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCredential
 - mfidl/IMFNetCredential
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredential
---

# IMFNetCredential interface


## -description

Sets and retrieves user-name and password information for authentication purposes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCredential</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetCredential</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCredential</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-getpassword">GetPassword</a>
</td>
<td align="left" width="63%">
Retrieves the decrypted password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-getuser">GetUser</a>
</td>
<td align="left" width="63%">
Retrieves the username.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-loggedonuser">LoggedOnUser</a>
</td>
<td align="left" width="63%">
Queries whether logged on credentials should be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser">SetUser</a>
</td>
<td align="left" width="63%">
Sets the user name.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>