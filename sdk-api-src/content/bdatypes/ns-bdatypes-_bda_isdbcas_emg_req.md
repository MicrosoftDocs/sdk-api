---
UID: NS:bdatypes._BDA_ISDBCAS_EMG_REQ
title: "_BDA_ISDBCAS_EMG_REQ"
author: windows-driver-content
description: Contains the data for an EMG command.
old-location: mstv\bda_isdbcas_emg_req.htm
old-project: mstv
ms.assetid: c622a840-9a08-40da-8fa5-6a0d668d23db
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PBDA_ISDBCAS_EMG_REQ, BDA_ISDBCAS_EMG_REQ, BDA_ISDBCAS_EMG_REQ structure [Microsoft TV Technologies], PBDA_ISDBCAS_EMG_REQ, PBDA_ISDBCAS_EMG_REQ structure pointer [Microsoft TV Technologies], _BDA_ISDBCAS_EMG_REQ, bdatypes/BDA_ISDBCAS_EMG_REQ, bdatypes/PBDA_ISDBCAS_EMG_REQ, mstv.bda_isdbcas_emg_req"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BDA_ISDBCAS_EMG_REQ, *PBDA_ISDBCAS_EMG_REQ
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdatypes.h
api_name:
-	BDA_ISDBCAS_EMG_REQ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BDA_ISDBCAS_EMG_REQ structure


## -description


Contains the data for an EMG command.

For more information, refer to ARIB STD-B25, <i>Conditional Access System Specifications For Digital Broadcasting</i>. (This resource may not be available in some languages 

and countries.)


## -struct-fields




### -field bCLA

The CLA (Class) byte. The value must be 0x90.


### -field bINS

The INS (Instruction) byte. The value must be 0x38.


### -field bP1

The P1 (Parameter 1) byte.


### -field bP2

The P2 (Parameter 2) byte.


### -field bLC

The size, in bytes, of the data that follows this structure member.


### -field bCardId

Card ID.


### -field bProtocol

Protocol number.


### -field bCABroadcasterGroupId

Broadcaster group identifier.


### -field bMessageControl

Message control.


### -field bMessageCode

Message code region. This array might be larger than the size given in the structure declaration. Use the value of <b>bLC</b> to determine the size.


## -see-also




<a href="https://msdn.microsoft.com/c93351f5-1829-4405-b665-00f2e78391e0">IBDA_ISDBConditionalAccess::SetIsdbCasRequest</a>
 

 

