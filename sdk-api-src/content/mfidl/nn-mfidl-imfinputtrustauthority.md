---
UID: NN:mfidl.IMFInputTrustAuthority
title: IMFInputTrustAuthority (mfidl.h)
author: windows-sdk-content
description: Enables other components in the protected media path (PMP) to use the input protection system provided by an input trust authorities (ITA).
old-location: mf\imfinputtrustauthority.htm
tech.root: medfound
ms.assetid: 637e0225-6fd8-4b83-b4fb-119e7a5ef5d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 637e0225-6fd8-4b83-b4fb-119e7a5ef5d2, IMFInputTrustAuthority, IMFInputTrustAuthority interface [Media Foundation], IMFInputTrustAuthority interface [Media Foundation],described, mf.imfinputtrustauthority, mfidl/IMFInputTrustAuthority
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFInputTrustAuthority"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFInputTrustAuthority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFInputTrustAuthority interface


## -description


Enables other components in the protected media path (PMP) to use the input protection system provided by an input trust authorities (ITA). An ITA is a component that implements an input protection system for media content. ITAs expose the <b>IMFInputTrustAuthority</b> interface.

An ITA translates policy from the content's native format into a common format that is used by other PMP components. It also provides a decrypter, if one is needed to decrypt the stream.

The topology contains one ITA instance for every protected stream in the media source. The ITA is obtained from the media source by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftrustedinput-getinputtrustauthority">IMFTrustedInput::GetInputTrustAuthority</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFInputTrustAuthority</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFInputTrustAuthority</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFInputTrustAuthority</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-bindaccess">BindAccess</a>
</td>
<td align="left" width="63%">
Notifies the ITA that a requested action is about to be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter">GetDecrypter</a>
</td>
<td align="left" width="63%">
Retrieves a decrypter transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getpolicy">GetPolicy</a>
</td>
<td align="left" width="63%">
Retrieves the policy that defines which output protection systems are allowed for this stream, and the configuration data for each protection system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-requestaccess">RequestAccess</a>
</td>
<td align="left" width="63%">
Requests permission to perform a specified action on the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the ITA to its initial state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-updateaccess">UpdateAccess</a>
</td>
<td align="left" width="63%">
Notifies the ITA when the number of output trust authorities (OTAs) that will perform a specified action has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

