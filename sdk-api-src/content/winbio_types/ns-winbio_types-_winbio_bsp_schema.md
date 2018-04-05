---
UID: NS:winbio_types._WINBIO_BSP_SCHEMA
title: "_WINBIO_BSP_SCHEMA"
author: windows-driver-content
description: Describes the capabilities of a biometric service provider.
old-location: secbiomet\winbio_bsp_schema.htm
old-project: SecBioMet
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BSP_SCHEMA, PWINBIO_BSP_SCHEMA, PWINBIO_BSP_SCHEMA structure pointer [Windows Biometric Framework API], WINBIO_BSP_SCHEMA, WINBIO_BSP_SCHEMA structure [Windows Biometric Framework API], _WINBIO_BSP_SCHEMA, secbiomet.winbio_bsp_schema, winbio_types/PWINBIO_BSP_SCHEMA, winbio_types/WINBIO_BSP_SCHEMA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h
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
req.typenames: WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BSP_SCHEMA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BSP_SCHEMA structure


## -description


The <b>WINBIO_BSP_SCHEMA</b> structure describes the capabilities of a biometric service provider. This structure is used by the <a href="https://msdn.microsoft.com/2424eae8-4fc6-43f4-97a1-3340870396cc">WinBioEnumServiceProviders</a> function.


## -struct-fields




### -field BiometricFactor

The type of biometric measurement used by this device. Currently this must be <b>WINBIO_TYPE_FINGERPRINT</b>.


### -field BspId

A value that uniquely identifies this biometric service provider component.


### -field Description

A <b>NULL</b>-terminated Unicode string that contains a description of the biometric service provider.


### -field Vendor

A <b>NULL</b>-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.


### -field Version

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536481">WINBIO_VERSION</a> structure the contains the software version of the biometric service provider component.


## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/2424eae8-4fc6-43f4-97a1-3340870396cc">WinBioEnumServiceProviders</a>
 

 

