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

# _NETLOGON_INFO_4 structure


## -description


The <b>NETLOGON_INFO_4</b> structure defines a level-4 control query response from a domain controller.


## -struct-fields




### -field netlog4_trusted_dc_name.string

 


### -field netlog4_trusted_domain_name.string

 


### -field netlog4_trusted_dc_name

A marshaled pointer to a string that contains the trusted domain controller name.


### -field netlog4_trusted_domain_name

A marshaled pointer to a string that contains the trusted domain name.


## -see-also




<a href="https://msdn.microsoft.com/bf40ee60-3a13-4a4e-a0f4-ba7c9fc11097">I_NetLogonControl2</a>
 

 

