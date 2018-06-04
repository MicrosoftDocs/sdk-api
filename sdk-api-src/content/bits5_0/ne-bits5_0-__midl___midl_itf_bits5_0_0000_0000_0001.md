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

# __MIDL___MIDL_itf_bits5_0_0000_0000_0001 enumeration


## -description


Enumeration that defines ID values corresponding to BITS properties.


## -enum-fields




### -field BITS_JOB_TRANSFER_POLICY_ALWAYS

Specifies that the job will be transferred when connectivity is available, regardless of the cost.


### -field BITS_JOB_TRANSFER_POLICY_NOT_ROAMING

Specifies that the job will be transferred when connectivity is available, unless that connectivity is subject to roaming surcharges.


### -field BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE

Specifies that the job will be transferred only when connectivity is available which is not subject to a surcharge.


### -field BITS_JOB_TRANSFER_POLICY_STANDARD

Specifies that the job will be transferred only when connectivity is available which is neither subject to a surcharge nor near exhaustion.


### -field BITS_JOB_TRANSFER_POLICY_UNRESTRICTED

Specifies that the job will be transferred only when connectivity is available which does not impose costs or traffic limits.

