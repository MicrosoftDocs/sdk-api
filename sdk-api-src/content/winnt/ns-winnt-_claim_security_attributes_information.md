---
UID: NS:winnt._CLAIM_SECURITY_ATTRIBUTES_INFORMATION
title: "_CLAIM_SECURITY_ATTRIBUTES_INFORMATION"
author: windows-sdk-content
description: Defines the security attributes for the claim.
old-location: security\claim_security_attributes_information.htm
old-project: SecAuthZ
ms.assetid: D7D9816E-1ECE-48CA-9F2F-0955572A0FCA
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PCLAIM_SECURITY_ATTRIBUTES_INFORMATION, CLAIM_SECURITY_ATTRIBUTES_INFORMATION, CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure [Security], PCLAIM_SECURITY_ATTRIBUTES_INFORMATION, PCLAIM_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security], _CLAIM_SECURITY_ATTRIBUTES_INFORMATION, security.claim_security_attributes_information, winnt/CLAIM_SECURITY_ATTRIBUTES_INFORMATION, winnt/PCLAIM_SECURITY_ATTRIBUTES_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CLAIM_SECURITY_ATTRIBUTES_INFORMATION, *PCLAIM_SECURITY_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	CLAIM_SECURITY_ATTRIBUTES_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure


## -description


The <b>CLAIM_SECURITY_ATTRIBUTES_INFORMATION</b> structure defines the security attributes for the claim. 


## -struct-fields




### -field Version

The version of the security attribute. This must be CLAIM_SECURITY_ATTRIBUTES_INFORMATION_VERSION_V1.


### -field Reserved

This member is currently reserved and must be zero when setting an attribute and is ignored when getting an attribute.


### -field AttributeCount

The number of values.


### -field Attribute

The actual attribute.


### -field Attribute.pAttributeV1

Pointer to an array that contains the <b>AttributeCount</b> member of the <a href="https://msdn.microsoft.com/FDBB9B00-01C3-474A-81FF-97C5CBA3261B">CLAIM_SECURITY_ATTRIBUTE_V1</a> structure.

