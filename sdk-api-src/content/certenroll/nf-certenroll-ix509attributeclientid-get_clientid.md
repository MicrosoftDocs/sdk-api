---
UID: NF:certenroll.IX509AttributeClientId.get_ClientId
title: IX509AttributeClientId::get_ClientId
author: windows-sdk-content
description: Retrieves the type of client application that generated the request.
old-location: security\ix509attributeclientid_clientid_property.htm
tech.root: seccertenroll
ms.assetid: 43073f84-28c6-4342-82ec-ca2289d51e02
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ClientId property [Security], ClientId property [Security],IX509AttributeClientId interface, IX509AttributeClientId interface [Security],ClientId property, IX509AttributeClientId.ClientId, IX509AttributeClientId.get_ClientId, IX509AttributeClientId::ClientId, IX509AttributeClientId::get_ClientId, certenroll/IX509AttributeClientId::ClientId, certenroll/IX509AttributeClientId::get_ClientId, get_ClientId, security.ix509attributeclientid_clientid_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IX509AttributeClientId.ClientId
 - IX509AttributeClientId.get_ClientId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeClientId::get_ClientId


## -description


The <b>ClientId</b> property retrieves the type of client application that generated the request.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/653b44fd-f69c-49e3-8aee-02445fa03cde">InitializeDecode</a> method to initialize the <b>ClientId</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/596682fc-aaf4-4247-a44b-34001cf7aecb">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd">ProcessName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a5a5027f-3854-4064-9cf7-675562b4cd57">UserSamName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>
 

 

