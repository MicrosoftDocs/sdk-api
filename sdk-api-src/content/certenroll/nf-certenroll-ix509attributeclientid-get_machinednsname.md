---
UID: NF:certenroll.IX509AttributeClientId.get_MachineDnsName
title: IX509AttributeClientId::get_MachineDnsName (certenroll.h)
description: Retrieves the Domain Name System (DNS) name of the computer that generated the request.
helpviewer_keywords: ["IX509AttributeClientId interface [Security]","MachineDnsName property","IX509AttributeClientId.MachineDnsName","IX509AttributeClientId.get_MachineDnsName","IX509AttributeClientId::MachineDnsName","IX509AttributeClientId::get_MachineDnsName","MachineDnsName property [Security]","MachineDnsName property [Security]","IX509AttributeClientId interface","certenroll/IX509AttributeClientId::MachineDnsName","certenroll/IX509AttributeClientId::get_MachineDnsName","get_MachineDnsName","security.ix509attributeclientid_machinednsname_property"]
old-location: security\ix509attributeclientid_machinednsname_property.htm
tech.root: security
ms.assetid: 596682fc-aaf4-4247-a44b-34001cf7aecb
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId interface [Security],MachineDnsName property, IX509AttributeClientId.MachineDnsName, IX509AttributeClientId.get_MachineDnsName, IX509AttributeClientId::MachineDnsName, IX509AttributeClientId::get_MachineDnsName, MachineDnsName property [Security], MachineDnsName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::MachineDnsName, certenroll/IX509AttributeClientId::get_MachineDnsName, get_MachineDnsName, security.ix509attributeclientid_machinednsname_property
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
 - IX509AttributeClientId::get_MachineDnsName
 - certenroll/IX509AttributeClientId::get_MachineDnsName
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
 - IX509AttributeClientId.MachineDnsName
 - IX509AttributeClientId.get_MachineDnsName
---

# IX509AttributeClientId::get_MachineDnsName


## -description

The <b>MachineDnsName</b> property retrieves the Domain Name System (DNS) name of the computer that generated the request.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> method to initialize the <b>MachineDnsName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>
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