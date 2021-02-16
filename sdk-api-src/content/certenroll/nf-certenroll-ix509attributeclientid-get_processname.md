---
UID: NF:certenroll.IX509AttributeClientId.get_ProcessName
title: IX509AttributeClientId::get_ProcessName (certenroll.h)
description: Retrieves the name of the application that generated the request.
helpviewer_keywords: ["IX509AttributeClientId interface [Security]","ProcessName property","IX509AttributeClientId.ProcessName","IX509AttributeClientId.get_ProcessName","IX509AttributeClientId::ProcessName","IX509AttributeClientId::get_ProcessName","ProcessName property [Security]","ProcessName property [Security]","IX509AttributeClientId interface","certenroll/IX509AttributeClientId::ProcessName","certenroll/IX509AttributeClientId::get_ProcessName","get_ProcessName","security.ix509attributeclientid_processname_property"]
old-location: security\ix509attributeclientid_processname_property.htm
tech.root: security
ms.assetid: 7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId interface [Security],ProcessName property, IX509AttributeClientId.ProcessName, IX509AttributeClientId.get_ProcessName, IX509AttributeClientId::ProcessName, IX509AttributeClientId::get_ProcessName, ProcessName property [Security], ProcessName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::ProcessName, certenroll/IX509AttributeClientId::get_ProcessName, get_ProcessName, security.ix509attributeclientid_processname_property
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
 - IX509AttributeClientId::get_ProcessName
 - certenroll/IX509AttributeClientId::get_ProcessName
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
 - IX509AttributeClientId.ProcessName
 - IX509AttributeClientId.get_ProcessName
---

# IX509AttributeClientId::get_ProcessName


## -description

The <b>ProcessName</b> property retrieves the name of the application that generated the request.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> method to initialize the <b>ProcessName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_machinednsname">MachineDnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_usersamname">UserSamName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>