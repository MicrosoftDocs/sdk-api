---
UID: NN:mfidl.IMFSecureChannel
title: IMFSecureChannel (mfidl.h)
description: Establishes a one-way secure channel between two objects.helpviewer_keywords: ["063170b8-9483-4acd-9b42-a226e9c38f0e","IMFSecureChannel","IMFSecureChannel interface [Media Foundation]","IMFSecureChannel interface [Media Foundation]","described","mf.imfsecurechannel","mfidl/IMFSecureChannel"]
old-location: mf\imfsecurechannel.htm
tech.root: medfound
ms.assetid: 063170b8-9483-4acd-9b42-a226e9c38f0e
ms.date: 12/05/2018
ms.keywords: 063170b8-9483-4acd-9b42-a226e9c38f0e, IMFSecureChannel, IMFSecureChannel interface [Media Foundation], IMFSecureChannel interface [Media Foundation],described, mf.imfsecurechannel, mfidl/IMFSecureChannel
f1_keywords:
- mfidl/IMFSecureChannel
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFSecureChannel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSecureChannel interface


## -description


Establishes a one-way secure channel between two objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSecureChannel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSecureChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSecureChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsecurechannel-getcertificate">GetCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the client's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsecurechannel-setupsession">SetupSession</a>
</td>
<td align="left" width="63%">
Passes the encrypted session key to the client.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

