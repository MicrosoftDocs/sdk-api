---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _CERT_POLICY_QUALIFIER_INFO structure


## -description


The <b>CERT_POLICY_QUALIFIER_INFO</b> structure contains an object identifier (OID) specifying the qualifier and qualifier-specific supplemental information.

The <b>CERT_POLICY_QUALIFIER_INFO</b> structure is a component of 
<a href="https://msdn.microsoft.com/0d6396fe-99f6-4f66-9f01-55582d24ddc1">CERT_POLICY_INFO</a>.


## -struct-fields




### -field pszPolicyQualifierId

OID specifying the qualifier.
					


### -field Qualifier

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains qualifier specific supplemental information.


## -see-also




<a href="https://msdn.microsoft.com/0d6396fe-99f6-4f66-9f01-55582d24ddc1">CERT_POLICY_INFO</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

