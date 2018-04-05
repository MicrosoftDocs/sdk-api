---
UID: NE:mfidl._MF_OPM_CGMSA_PROTECTION_LEVEL
title: "_MF_OPM_CGMSA_PROTECTION_LEVEL"
author: windows-driver-content
description: Defines protection levels for MFPROTECTION_CGMSA.
old-location: mf\mf_opm_cgmsa_protection_level.htm
old-project: medfound
ms.assetid: EEFE04F7-E878-4F09-B973-B0FD3E9431AA
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MF_OPM_CGMSA_COPY_FREELY, MF_OPM_CGMSA_COPY_NEVER, MF_OPM_CGMSA_COPY_NO_MORE, MF_OPM_CGMSA_COPY_ONE_GENERATION, MF_OPM_CGMSA_OFF, MF_OPM_CGMSA_PROTECTION_LEVEL, MF_OPM_CGMSA_PROTECTION_LEVEL enumeration [Media Foundation], MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED, _MF_OPM_CGMSA_PROTECTION_LEVEL, mf.mf_opm_cgmsa_protection_level, mfidl/MF_OPM_CGMSA_COPY_FREELY, mfidl/MF_OPM_CGMSA_COPY_NEVER, mfidl/MF_OPM_CGMSA_COPY_NO_MORE, mfidl/MF_OPM_CGMSA_COPY_ONE_GENERATION, mfidl/MF_OPM_CGMSA_OFF, mfidl/MF_OPM_CGMSA_PROTECTION_LEVEL, mfidl/MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_OPM_CGMSA_PROTECTION_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	MF_OPM_CGMSA_PROTECTION_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF_OPM_CGMSA_PROTECTION_LEVEL enumeration


## -description


Defines protection levels for <b>MFPROTECTION_CGMSA</b>.


## -enum-fields




### -field MF_OPM_CGMSA_OFF

CGMS-A is disabled.


### -field MF_OPM_CGMSA_COPY_FREELY

The protection level is Copy Freely.


### -field MF_OPM_CGMSA_COPY_NO_MORE

The protection level is Copy No More.


### -field MF_OPM_CGMSA_COPY_ONE_GENERATION

The protection level is Copy One Generation.


### -field MF_OPM_CGMSA_COPY_NEVER

The protection level is Copy Never.


### -field MF_OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED

Redistribution control (also called the broadcast flag) is required. This flag can be combined with the other flags.


## -remarks



These flags are equivalent to the OPM_CGMSA_Protection_Level enumeration constants used in the Output Protection Protocol (OPM). 




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

