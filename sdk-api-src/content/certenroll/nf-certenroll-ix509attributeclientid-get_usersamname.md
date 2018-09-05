---
UID: NF:certenroll.IX509AttributeClientId.get_UserSamName
title: IX509AttributeClientId::get_UserSamName
author: windows-sdk-content
description: Retrieves the Security Accounts Manager (SAM) name of the user.
old-location: security\ix509attributeclientid_usersamname_property.htm
old-project: SecCertEnroll
ms.assetid: a5a5027f-3854-4064-9cf7-675562b4cd57
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509AttributeClientId interface [Security],UserSamName property, IX509AttributeClientId.UserSamName, IX509AttributeClientId.get_UserSamName, IX509AttributeClientId::UserSamName, IX509AttributeClientId::get_UserSamName, UserSamName property [Security], UserSamName property [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::UserSamName, certenroll/IX509AttributeClientId::get_UserSamName, get_UserSamName, security.ix509attributeclientid_usersamname_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeClientId::get_UserSamName


## -description


The <b>UserSamName</b> property retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) name of the user.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/653b44fd-f69c-49e3-8aee-02445fa03cde">InitializeDecode</a> method to initialize the <b>UserSamName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/43073f84-28c6-4342-82ec-ca2289d51e02">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/596682fc-aaf4-4247-a44b-34001cf7aecb">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd">ProcessName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>
 

 

