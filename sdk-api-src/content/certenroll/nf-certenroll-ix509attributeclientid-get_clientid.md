---
UID: NF:certenroll.IX509AttributeClientId.get_ClientId
title: IX509AttributeClientId::get_ClientId (certenroll.h)
description: Retrieves the type of client application that generated the request.
helpviewer_keywords: ["ClientId property [Security]","ClientId property [Security]","IX509AttributeClientId interface","IX509AttributeClientId interface [Security]","ClientId property","IX509AttributeClientId.ClientId","IX509AttributeClientId.get_ClientId","IX509AttributeClientId::ClientId","IX509AttributeClientId::get_ClientId","certenroll/IX509AttributeClientId::ClientId","certenroll/IX509AttributeClientId::get_ClientId","get_ClientId","security.ix509attributeclientid_clientid_property"]
old-location: security\ix509attributeclientid_clientid_property.htm
tech.root: security
ms.assetid: 43073f84-28c6-4342-82ec-ca2289d51e02
ms.date: 12/05/2018
ms.keywords: ClientId property [Security], ClientId property [Security],IX509AttributeClientId interface, IX509AttributeClientId interface [Security],ClientId property, IX509AttributeClientId.ClientId, IX509AttributeClientId.get_ClientId, IX509AttributeClientId::ClientId, IX509AttributeClientId::get_ClientId, certenroll/IX509AttributeClientId::ClientId, certenroll/IX509AttributeClientId::get_ClientId, get_ClientId, security.ix509attributeclientid_clientid_property
req.header: certenroll.h
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509AttributeClientId::get_ClientId
 - certenroll/IX509AttributeClientId::get_ClientId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeClientId.ClientId
 - IX509AttributeClientId.get_ClientId
---

# IX509AttributeClientId::get_ClientId


## -description

The <b>ClientId</b> property retrieves the type of client application that generated the request.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> method to initialize the <b>ClientId</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_machinednsname">MachineDnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_processname">ProcessName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_usersamname">UserSamName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>