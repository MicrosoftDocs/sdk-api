---
UID: NF:certenroll.IX509AttributeClientId.get_UserSamName
title: IX509AttributeClientId::get_UserSamName
author: windows-sdk-content
description: Retrieves the Security Accounts Manager (SAM) name of the user.
old-location: security\ix509attributeclientid_usersamname_property.htm
old-project: seccertenroll
ms.assetid: a5a5027f-3854-4064-9cf7-675562b4cd57
ms.author: windowssdkdev
ms.date: 07/30/2018
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


The <b>UserSamName</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Security Accounts Manager</a> (SAM) name of the user.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377076(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377075(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>UserSamName</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377074(v=VS.85).aspx">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377077(v=VS.85).aspx">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377079(v=VS.85).aspx">ProcessName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>
 

 

