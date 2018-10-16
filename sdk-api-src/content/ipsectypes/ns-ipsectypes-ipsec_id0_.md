---
UID: NS:ipsectypes.IPSEC_ID0_
title: IPSEC_ID0_
author: windows-sdk-content
description: Contains information corresponding to identities that are authenticated by IPsec.
old-location: fwp\ipsec_id0.htm
tech.root: fwp
ms.assetid: e8881c50-9586-447e-a514-cc28895e5e90
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPSEC_ID0, IPSEC_ID0 structure [Filtering], IPSEC_ID0_, fwp.ipsec_id0, ipsectypes/IPSEC_ID0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_ID0
product: Windows
targetos: Windows
req.typenames: IPSEC_ID0
req.redist: 
---

# IPSEC_ID0_ structure


## -description


The <b>IPSEC_ID0</b> structure  contains information corresponding to identities that are authenticated by IPsec.


## -struct-fields




### -field mmTargetName

Optional main mode target service principal name (SPN).  This is often the machine name.


### -field emTargetName

Optional extended mode target SPN.


### -field numTokens

Optional.  Number of <a href="https://msdn.microsoft.com/12adf88e-05c7-4e08-bbf7-6da529387af1">IPSEC_TOKEN0</a> structures present in the <b>tokens</b> member.


### -field tokens

Optional array of <a href="https://msdn.microsoft.com/12adf88e-05c7-4e08-bbf7-6da529387af1">IPSEC_TOKEN0</a> structures.


### -field explicitCredentials

Optional handle to explicit credentials.


### -field logonId

Unused parameter. This should always be 0.


## -remarks



<b>IPSEC_ID0</b> is a specific implementation of IPSEC_ID. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

