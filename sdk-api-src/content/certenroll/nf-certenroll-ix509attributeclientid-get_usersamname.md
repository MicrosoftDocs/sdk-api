---
UID: NF:certenroll.IX509AttributeClientId.get_UserSamName
title: IX509AttributeClientId::get_UserSamName (certenroll.h)
author: windows-sdk-content
description: Retrieves the Security Accounts Manager (SAM) name of the user.
old-location: security\ix509attributeclientid_usersamname_property.htm
tech.root: seccertenroll
ms.assetid: a5a5027f-3854-4064-9cf7-675562b4cd57
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId interface [Security],UserSamName property, IX509AttributeClientId.UserSamName, IX509AttributeClientId.get_UserSamName, IX509AttributeClientId::UserSamName, IX509AttributeClientId::get_UserSamName, UserSamName property [Security], UserSamName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::UserSamName, certenroll/IX509AttributeClientId::get_UserSamName, get_UserSamName, security.ix509attributeclientid_usersamname_property
ms.topic: method
f1_keywords: 
 - "certenroll/IX509AttributeClientId.UserSamName"
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
 - IX509AttributeClientId.UserSamName
 - IX509AttributeClientId.get_UserSamName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeClientId::get_UserSamName


## -description


The <b>UserSamName</b> property retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) name of the user.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a> method or the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> method to initialize the <b>UserSamName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_machinednsname">MachineDnsName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_processname">ProcessName</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>
 

 

