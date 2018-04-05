---
UID: NE:ksmedia._TunerDecoderLockType
title: "_TunerDecoderLockType"
author: windows-driver-content
description: The TunerLockType enumeration type specifies how well a television tuner has locked onto a signal.
old-location: mstv\tunerlocktype.htm
old-project: mstv
ms.assetid: 657dfd46-b01c-41aa-af0c-0d07235f15fc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: TunerLockType, TunerLockType enumeration [Microsoft TV Technologies], Tuner_LockType_Locked, Tuner_LockType_None, Tuner_LockType_Within_Scan_Sensing_Range, _TunerDecoderLockType, ksmedia/TunerLockType, ksmedia/Tuner_LockType_Locked, ksmedia/Tuner_LockType_None, ksmedia/Tuner_LockType_Within_Scan_Sensing_Range, mstv.tunerlocktype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ksmedia.h
req.include-header: 
req.target-type: Windows
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
req.typenames: TunerLockType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ksmedia.h
api_name:
-	TunerLockType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _TunerDecoderLockType enumeration


## -description



The <b>TunerLockType</b> enumeration type specifies how well a television tuner has locked onto a signal.




## -enum-fields




### -field Tuner_LockType_None

The tuner is not locked onto a signal. If this value is returned at the end of a scan, it means the tuner was not able to lock onto a signal anywhere within the scanning range.


### -field Tuner_LockType_Within_Scan_Sensing_Range

The tuner found a signal in the vicinity but could establish the exact frequency.


### -field Tuner_LockType_Locked

The tuner locked onto an exact frequency. This value indicates that the tuner was able to fine tune to a frequency.


## -see-also




<a href="https://msdn.microsoft.com/13183e2a-6fbb-422c-b93c-53c12cb27423">BDA Enumeration Types</a>
 

 

