---
UID: NF:certenroll.IX509AttributeClientId.get_ClientId
title: IX509AttributeClientId::get_ClientId
author: windows-sdk-content
description: Retrieves the type of client application that generated the request.
old-location: security\ix509attributeclientid_clientid_property.htm
tech.root: SecCertEnroll
ms.assetid: 43073f84-28c6-4342-82ec-ca2289d51e02
ms.author: windowssdkdev
ms.date: 09/26/2018
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



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377076(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377075(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>ClientId</b> value. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377077(v=VS.85).aspx">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377079(v=VS.85).aspx">ProcessName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377081(v=VS.85).aspx">UserSamName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>
 

 

