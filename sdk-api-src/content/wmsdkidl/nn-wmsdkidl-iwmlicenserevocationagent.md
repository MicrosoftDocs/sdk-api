---
UID: NN:wmsdkidl.IWMLicenseRevocationAgent
title: IWMLicenseRevocationAgent (wmsdkidl.h)
description: The IWMLicenseRevocationAgent interface handles messages from a DRM license server that involve license revocation.IWMLicenseRevocationAgent is the primary interface of the license revocation agent object.
helpviewer_keywords: ["IWMLicenseRevocationAgent","IWMLicenseRevocationAgent interface [windows Media Format]","IWMLicenseRevocationAgent interface [windows Media Format]","described","IWMLicenseRevocationAgentInterface","wmformat.iwmlicenserevocationagent","wmsdkidl/IWMLicenseRevocationAgent"]
old-location: wmformat\iwmlicenserevocationagent.htm
tech.root: wmformat
ms.assetid: 4cb5beb9-72b8-46cb-8460-56455785a7a0
ms.date: 12/05/2018
ms.keywords: IWMLicenseRevocationAgent, IWMLicenseRevocationAgent interface [windows Media Format], IWMLicenseRevocationAgent interface [windows Media Format],described, IWMLicenseRevocationAgentInterface, wmformat.iwmlicenserevocationagent, wmsdkidl/IWMLicenseRevocationAgent
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
 - IWMLicenseRevocationAgent
 - wmsdkidl/IWMLicenseRevocationAgent
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
 - IWMLicenseRevocationAgent
---

# IWMLicenseRevocationAgent interface


## -description

The <b>IWMLicenseRevocationAgent</b> interface handles messages from a DRM license server that involve license revocation.

<b>IWMLicenseRevocationAgent</b> is the primary interface of the license revocation agent object. You can create an instance of the object and retrieve a pointer to its <b>IWMLicenseRevocationAgent</b> interface by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent">WMCreateLicenseRevocationAgent</a> function.

## -inheritance

The <b>IWMLicenseRevocationAgent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLicenseRevocationAgent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

License revocation enables a license issuer to remove licenses from a computer.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
