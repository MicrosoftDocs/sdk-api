---
UID: NE:opmapi._OPM_ACP_PROTECTION_LEVEL
title: "_OPM_ACP_PROTECTION_LEVEL"
author: windows-driver-content
description: Specifies the protection level for Analog Copy Protection (ACP).
old-location: mf\opm_acp_protection_level.htm
old-project: medfound
ms.assetid: f52b4ee6-1ab3-4153-86e3-5ae69fd8a958
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: OPM_ACP_FORCE_ULONG, OPM_ACP_LEVEL_ONE, OPM_ACP_LEVEL_THREE, OPM_ACP_LEVEL_TWO, OPM_ACP_OFF, OPM_ACP_PROTECTION_LEVEL, OPM_ACP_PROTECTION_LEVEL enumeration [Media Foundation], _OPM_ACP_PROTECTION_LEVEL, mf.opm_acp_protection_level, opmapi/OPM_ACP_FORCE_ULONG, opmapi/OPM_ACP_LEVEL_ONE, opmapi/OPM_ACP_LEVEL_THREE, opmapi/OPM_ACP_LEVEL_TWO, opmapi/OPM_ACP_OFF, opmapi/OPM_ACP_PROTECTION_LEVEL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: opmapi.h
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
req.typenames: OPM_ACP_PROTECTION_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	opmapi.h
api_name:
-	OPM_ACP_PROTECTION_LEVEL
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _OPM_ACP_PROTECTION_LEVEL enumeration


## -description


Specifies the protection level for Analog Copy Protection (ACP).


## -enum-fields




### -field OPM_ACP_OFF

ACP is disabled.


### -field OPM_ACP_LEVEL_ONE

ACP protection level 1.


### -field OPM_ACP_LEVEL_TWO

ACP protection level 2.


### -field OPM_ACP_LEVEL_THREE

ACP protection level 3.


### -field OPM_ACP_FORCE_ULONG

Reserved.


## -remarks



This enumeration is numerically equivalent to the <b>COPP_ACP_Protection_Level</b> enumeration used in Certified Output Protection Protocol. The OPM_ACP_OFF flag corresponds to COPP_ACP_Level0.




## -see-also




<a href="https://msdn.microsoft.com/e72e0a5e-476d-41f0-9139-54c4c488053f">OPM Enumerations</a>
 

 

