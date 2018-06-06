---
UID: NE:ntdsapi.DS_NAME_FLAGS
title: DS_NAME_FLAGS
author: windows-sdk-content
description: The DS_NAME_FLAGS enumeration is used to define how the name syntax will be cracked. These flags are used by the DsCrackNames function.
old-location: ad\ds_name_flags.htm
old-project: AD
ms.assetid: f0108568-4a6a-4159-b55f-2c651c588b73
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DS_NAME_FLAGS, DS_NAME_FLAGS enumeration [Active Directory], DS_NAME_FLAG_EVAL_AT_DC, DS_NAME_FLAG_GCVERIFY, DS_NAME_FLAG_SYNTACTICAL_ONLY, DS_NAME_FLAG_TRUST_REFERRAL, DS_NAME_NO_FLAGS, _glines_ds_name_flags, ad.ds__name__flags, ad.ds_name_flags, ntdsapi/DS_NAME_FLAGS, ntdsapi/DS_NAME_FLAG_EVAL_AT_DC, ntdsapi/DS_NAME_FLAG_GCVERIFY, ntdsapi/DS_NAME_FLAG_SYNTACTICAL_ONLY, ntdsapi/DS_NAME_FLAG_TRUST_REFERRAL, ntdsapi/DS_NAME_NO_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DS_NAME_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_NAME_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
---

# DS_NAME_FLAGS enumeration


## -description


The <b>DS_NAME_FLAGS</b> enumeration is used to define how the name syntax will be cracked. These flags are used by the <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> function.


## -enum-fields




### -field DS_NAME_NO_FLAGS

Indicates that there are no associated flags.


### -field DS_NAME_FLAG_SYNTACTICAL_ONLY

Performs a syntactical mapping at the client without transferring over the network. The only syntactic mapping supported is from <a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_FQDN_1779_NAME</a> to <b>DS_CANONICAL_NAME</b> or <b>DS_CANONICAL_NAME_EX</b>. <a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a> returns the <b>DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING</b> flag if a  syntactical mapping is not possible.


### -field DS_NAME_FLAG_EVAL_AT_DC

Forces a trip to the domain controller for evaluation, even if the syntax could be cracked locally.


### -field DS_NAME_FLAG_GCVERIFY

The call fails if the domain controller is not a global catalog server.


### -field DS_NAME_FLAG_TRUST_REFERRAL

Enables cross forest trust referral.


## -see-also




<a href="https://msdn.microsoft.com/7a99e531-5a38-4352-8921-7b5a765ffd03">DS_NAME_FORMAT</a>



<a href="https://msdn.microsoft.com/f812a001-5aab-4c62-87bd-54f95792e271">DsCrackNames</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

