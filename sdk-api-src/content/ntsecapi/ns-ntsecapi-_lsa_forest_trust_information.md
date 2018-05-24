---
UID: NS:ntsecapi._LSA_FOREST_TRUST_INFORMATION
title: "_LSA_FOREST_TRUST_INFORMATION"
author: windows-driver-content
description: Contains Local Security Authority forest trust information.
old-location: security\lsa_forest_trust_information.htm
old-project: SecAuthN
ms.assetid: 9e456462-59a9-4f18-ba47-92fc2350889b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PLSA_FOREST_TRUST_INFORMATION, LSA_FOREST_TRUST_INFORMATION, LSA_FOREST_TRUST_INFORMATION structure [Security], PLSA_FOREST_TRUST_INFORMATION, PLSA_FOREST_TRUST_INFORMATION structure pointer [Security], _LSA_FOREST_TRUST_INFORMATION, ntsecapi/LSA_FOREST_TRUST_INFORMATION, ntsecapi/PLSA_FOREST_TRUST_INFORMATION, security.lsa_forest_trust_information"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LSA_FOREST_TRUST_INFORMATION, *PLSA_FOREST_TRUST_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	LSA_FOREST_TRUST_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _LSA_FOREST_TRUST_INFORMATION structure


## -description


The <b>LSA_FOREST_TRUST_INFORMATION</b> structure contains <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust information.


## -struct-fields




### -field RecordCount.range

 


### -field RecordCount.range.0

 


### -field RecordCount.range.MAX_RECORDS_IN_FOREST_TRUST_INFO

 


### -field Entries.size_is

 


### -field Entries.size_is.RecordCount

 


### -field RecordCount

Number of <a href="https://msdn.microsoft.com/19b4ee56-664f-4f37-bfc9-129032ebeb22">LSA_FOREST_TRUST_RECORD</a> structures in the array pointed to by the <b>Entries</b> member.


### -field Entries

Pointer to a pointer to an array of <a href="https://msdn.microsoft.com/19b4ee56-664f-4f37-bfc9-129032ebeb22">LSA_FOREST_TRUST_RECORD</a> structures, each of which contains one piece of forest trust information.

