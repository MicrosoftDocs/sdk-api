---
UID: NE:comsvcs.tagCRMREGFLAGS
title: tagCRMREGFLAGS
author: windows-sdk-content
description: Controls which phases of transaction completion should be received by the CRM compensator and whether recovery should fail if in-doubt transactions remain after recovery has been attempted.
old-location: cos\crmregflags.htm
tech.root: cossdk
ms.assetid: 94178edf-fd0d-4d8d-8bf8-ced17f65d82f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CRMREGFLAGS, CRMREGFLAGS enumeration [COM+], CRMREGFLAG_ABORTPHASE, CRMREGFLAG_ALLPHASES, CRMREGFLAG_COMMITPHASE, CRMREGFLAG_FAILIFINDOUBTSREMAIN, CRMREGFLAG_PREPAREPHASE, _cos_CRMREGFLAGS, comsvcs/CRMREGFLAGS, comsvcs/CRMREGFLAG_ABORTPHASE, comsvcs/CRMREGFLAG_ALLPHASES, comsvcs/CRMREGFLAG_COMMITPHASE, comsvcs/CRMREGFLAG_FAILIFINDOUBTSREMAIN, comsvcs/CRMREGFLAG_PREPAREPHASE, cos.crmregflags, tagCRMREGFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - ComSvcs.h
api_name:
 - CRMREGFLAGS
product: Windows
targetos: Windows
req.typenames: CRMREGFLAGS
req.redist: 
---

# tagCRMREGFLAGS enumeration


## -description


Controls which phases of transaction completion should be received by the CRM compensator and whether recovery should fail if in-doubt transactions remain after recovery has been attempted.


## -enum-fields




### -field CRMREGFLAG_PREPAREPHASE

Receive the prepare phase.


### -field CRMREGFLAG_COMMITPHASE

Receive the commit phase.


### -field CRMREGFLAG_ABORTPHASE

Receive the abort phase.


### -field CRMREGFLAG_ALLPHASES

Receive all phases.


### -field CRMREGFLAG_FAILIFINDOUBTSREMAIN

Fail if in-doubt transactions remain after recovery.


## -see-also




<a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">ICrmLogControl::RegisterCompensator</a>
 

 

