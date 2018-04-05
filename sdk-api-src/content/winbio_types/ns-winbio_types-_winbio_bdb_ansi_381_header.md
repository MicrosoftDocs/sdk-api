---
UID: NS:winbio_types._WINBIO_BDB_ANSI_381_HEADER
title: "_WINBIO_BDB_ANSI_381_HEADER"
author: windows-driver-content
description: Specifies information about a series of fingerprint or palm samples.
old-location: secbiomet\winbio_bdb_ansi_381_header.htm
old-project: SecBioMet
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BDB_ANSI_381_HEADER, WINBIO_BDB_ANSI_381_HEADER, WINBIO_BDB_ANSI_381_HEADER structure [Windows Biometric Framework API], _WINBIO_BDB_ANSI_381_HEADER, secbiomet.winbio_bdb_ansi_381_header, winbio_types/WINBIO_BDB_ANSI_381_HEADER"
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
req.typenames: WINBIO_BDB_ANSI_381_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BDB_ANSI_381_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BDB_ANSI_381_HEADER structure


## -description


The <b>WINBIO_BDB_ANSI_381_HEADER</b> structure specifies information about a series of fingerprint or palm samples.


## -struct-fields




### -field RecordLength

The size, in bytes, of this structure plus the size of all <a href="https://msdn.microsoft.com/e0b32d05-3e96-4b42-9e18-57d10513f224">WINBIO_BDB_ANSI_381_RECORD</a> structures for the fingerprint or palm samples captured from an end user. Only the low six bytes are valid.


### -field FormatIdentifier

Specifies the format. Currently, this must be 0x46495200.


### -field VersionNumber

Specifies the version number. Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.


### -field ProductId

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536473">WINBIO_REGISTERED_FORMAT</a> structure that contains the registered data format as an owner/type pair.


### -field CaptureDeviceId

Contains the unit ID of the device used to capture the sample.


### -field ImageAcquisitionLevel

Specifies the resolution level at which the sample is captured.


### -field HorizontalScanResolution

Specifies the horizontal resolution of the scan.


### -field VerticalScanResolution

Specifies the vertical resolution of the scan.


### -field HorizontalImageResolution

Specifies the horizontal resolution of the captured fingerprint or palm image.


### -field VerticalImageResolution

Specifies the vertical resolution of the captured fingerprint or palm image.


### -field ElementCount

Number of finger or palm records in this structure.


### -field ScaleUnits

Contains the unit of measure, 1 for inches and 2 for centimeters.


### -field PixelDepth

Specifies the number of bits in a pixel. This can be 1 to 16 bits per pixel for color.


### -field ImageCompressionAlg

Specifies the algorithm used to compress the finger or palm image.


### -field Reserved


## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>
 

 

