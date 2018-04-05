---
UID: NS:winbio_types._WINBIO_BIR
title: "_WINBIO_BIR"
author: windows-driver-content
description: Represents a biometric information record (BIR).
old-location: secbiomet\winbio_bir.htm
old-project: SecBioMet
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BIR, WINBIO_BIR, WINBIO_BIR structure [Windows Biometric Framework API], _WINBIO_BIR, secbiomet.winbio_bir, winbio_types/WINBIO_BIR"
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
req.typenames: WINBIO_BIR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BIR structure


## -description


The <b>WINBIO_BIR</b> structure represents a biometric information record (BIR). The information record contains header, data, and signature blocks.


## -struct-fields




### -field HeaderBlock

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536460">WINBIO_BIR_DATA</a> structure that contains the size, in bytes, and offset of the BIR header. The header contains information that describes the contents of the information record.


### -field StandardDataBlock

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536460">WINBIO_BIR_DATA</a> structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).


### -field VendorDataBlock

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536460">WINBIO_BIR_DATA</a> structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by  vendor sensors and software.


### -field SignatureBlock

An optional  <a href="https://msdn.microsoft.com/library/windows/hardware/ff536460">WINBIO_BIR_DATA</a> structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR. If present, the signature or MAC must cover the header and data blocks.


## -remarks



The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.

The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.

If this structure contains a <i>StandardDataBlock</i> value, the <i>Type</i> parameter of the header specified by the <i>HeaderBlock</i> parameter must be set to  <b>WINBIO_ANSI_381_FORMAT_TYPE</b>. This is the only standard data format supported by the current version of the Windows Biometric Framework.




## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536460">WINBIO_BIR_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536462">WINBIO_BIR_HEADER</a>
 

 

