---
UID: NF:certenroll.IX509AttributeClientId.get_MachineDnsName
title: IX509AttributeClientId::get_MachineDnsName (certenroll.h)
description: Retrieves the Domain Name System (DNS) name of the computer that generated the request.
old-location: security\ix509attributeclientid_machinednsname_property.htm
tech.root: seccertenroll
ms.assetid: 596682fc-aaf4-4247-a44b-34001cf7aecb
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId interface [Security],MachineDnsName property, IX509AttributeClientId.MachineDnsName, IX509AttributeClientId.get_MachineDnsName, IX509AttributeClientId::MachineDnsName, IX509AttributeClientId::get_MachineDnsName, MachineDnsName property [Security], MachineDnsName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::MachineDnsName, certenroll/IX509AttributeClientId::get_MachineDnsName, get_MachineDnsName, security.ix509attributeclientid_machinednsname_property
ms.topic: method
f1_keywords:
- certenroll/IX509AttributeClientId.MachineDnsName
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeClientId::get_MachineDnsName


## -description


The <b>MachineDnsName</b> property retrieves the Domain Name System (DNS) name of the computer that generated the request.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a> method or the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> method to initialize the <b>MachineDnsName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_processname">ProcessName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_usersamname">UserSamName</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>
 

 

