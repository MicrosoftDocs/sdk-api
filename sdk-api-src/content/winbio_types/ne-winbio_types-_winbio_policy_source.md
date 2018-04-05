---
UID: NE:winbio_types._WINBIO_POLICY_SOURCE
title: "_WINBIO_POLICY_SOURCE"
author: windows-driver-content
description: Lists the possible sources of policy information for the detection of spoofing for biometric factors.
old-location: secbiomet\winbio_policy_source.htm
old-project: SecBioMet
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_POLICY_SOURCE, PWINBIO_POLICY_SOURCE, PWINBIO_POLICY_SOURCE enumeration pointer [Windows Biometric Framework API], WINBIO_POLICY_ADMIN, WINBIO_POLICY_DEFAULT, WINBIO_POLICY_LOCAL, WINBIO_POLICY_SOURCE, WINBIO_POLICY_SOURCE enumeration [Windows Biometric Framework API], WINBIO_POLICY_UNKNOWN, _WINBIO_POLICY_SOURCE, secbiomet.winbio_policy_source, winbio_types/PWINBIO_POLICY_SOURCE, winbio_types/WINBIO_POLICY_ADMIN, winbio_types/WINBIO_POLICY_DEFAULT, winbio_types/WINBIO_POLICY_LOCAL, winbio_types/WINBIO_POLICY_SOURCE, winbio_types/WINBIO_POLICY_UNKNOWN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winbio_types.h
req.include-header: Winbio.h for client applications or Winbio_adapters.h for adapters
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_types.h
api_name:
-	WINBIO_POLICY_SOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_POLICY_SOURCE enumeration


## -description


Lists the possible sources of policy information for the detection of spoofing for biometric factors.


## -enum-fields




### -field WINBIO_POLICY_UNKNOWN

The source of the policy is unknown.


### -field WINBIO_POLICY_DEFAULT

The policy is the default policy that the Windows Biometric Framework provides.


### -field WINBIO_POLICY_LOCAL

The policy that the individual user set for their account by using the <b>Settings</b> app. This policy overrides the default policy.


### -field WINBIO_POLICY_ADMIN

A group policy that the IT administrator set for the enterprise. Individual users cannot override this policy.


## -see-also




<a href="https://msdn.microsoft.com/846C0725-1796-49E4-883C-44AC7D618317">WINBIO_ANTI_SPOOF_POLICY_ACTION</a>
 

 

