---
UID: NS:winbio_ioctl._WINBIO_DATA
title: "_WINBIO_DATA"
author: windows-driver-content
description: The WINBIO_DATA structure specifies data in IOCTL payloads.
old-location: biometric\winbio_data.htm
old-project: biometric
ms.assetid: 00dc716c-621f-4312-bf53-6bc3ab492faa
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: "*PWINBIO_DATA, PWINBIO_DATA, PWINBIO_DATA structure pointer [Biometric Devices], WINBIO_DATA, WINBIO_DATA structure [Biometric Devices], _WINBIO_DATA, biometric.winbio_data, biometric_ref_1d08ec8c-d73e-462f-a2f3-dce508bc159f.xml, winbio_ioctl/PWINBIO_DATA, winbio_ioctl/WINBIO_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_ioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
req.typenames: WINBIO_DATA, *PWINBIO_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_ioctl.h
api_name:
-	WINBIO_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_DATA structure


## -description


The WINBIO_DATA structure specifies data in IOCTL payloads.


## -struct-fields




### -field Size

Specifies the size, in bytes, of the payload.


### -field Data

Specifies an array that contains the payload. Frequently this member contains a structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a>.


## -remarks



The WINBIO_DATA structure associates a length, in bytes, with an arbitrary block of contiguous memory.



