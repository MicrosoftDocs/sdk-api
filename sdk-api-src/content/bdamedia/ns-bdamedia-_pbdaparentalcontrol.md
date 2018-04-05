---
UID: NS:bdamedia._PBDAParentalControl
title: "_PBDAParentalControl"
author: windows-driver-content
description: Specifies the parental control policy for a digital television program.
old-location: mstv\pbdaparentalcontrol.htm
old-project: mstv
ms.assetid: 4086651b-45b3-4896-9ae2-6db7e121eb5e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: PBDAParentalControl, PBDAParentalControl structure [Microsoft TV Technologies], _PBDAParentalControl, bdamedia/PBDAParentalControl, mstv.pbdaparentalcontrol
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
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
req.typenames: PBDAParentalControl
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	PBDAParentalControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _PBDAParentalControl structure


## -description


Specifies the parental control policy for a digital television program.


## -struct-fields




### -field rating_system_count

 


### -field rating_systems

 




#### - ulEndTime

The end time when parental access is longer required, in seconds from midnight.


#### - ulPolicy

A member of the <a href="https://msdn.microsoft.com/bfd9da34-50e4-4e67-a17e-9f6366e5ef46">PBDAParentalControlPolicy</a> enumeration.


#### - ulStartTime

The start time when parental access is required, in seconds from midnight.


## -remarks



If parental access is not required, the <b>ulStartTime</b> and <b>ulEndTime</b> members are set to -1.



