---
UID: NS:winbio_types._WINBIO_REGISTERED_FORMAT
title: "_WINBIO_REGISTERED_FORMAT"
author: windows-driver-content
description: Specifies a registered data format as an owner/format pair.
old-location: secbiomet\winbio_registered_format.htm
old-project: SecBioMet
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_REGISTERED_FORMAT, PWINBIO_REGISTERED_FORMAT, PWINBIO_REGISTERED_FORMAT structure pointer [Windows Biometric Framework API], WINBIO_REGISTERED_FORMAT, WINBIO_REGISTERED_FORMAT structure [Windows Biometric Framework API], _WINBIO_REGISTERED_FORMAT, secbiomet.winbio_registered_format, winbio_types/PWINBIO_REGISTERED_FORMAT, winbio_types/WINBIO_REGISTERED_FORMAT"
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
req.typenames: WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_REGISTERED_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_REGISTERED_FORMAT structure


## -description


The <b>WINBIO_REGISTERED_FORMAT</b> structure specifies a registered data format as an owner/format pair.


## -struct-fields




### -field Owner

An IBIA (International Biometric Industry Association) assigned owner value.


### -field Type

An owner assigned format.


## -remarks



Because Windows currently supports only fingerprint readers, the following values should be used in the <b>WINBIO_REGISTERED_FORMAT</b> structure.

<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WINBIO_ANSI_381_FORMAT_OWNER

</td>
<td>
InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).

</td>
</tr>
<tr>
<td>
WINBIO_ANSI_381_FORMAT_TYPE

</td>
<td>
ANSI INCITS 381 finger image based data interchange format.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/5EFFF7EB-D998-4EE9-A23F-B17477F00863">WINBIO_ANSI_381_FORMAT Constants</a>



<a href="https://msdn.microsoft.com/8b0caa50-9bba-45c4-b4bf-514540894793">WINBIO_BDB_ANSI_381_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536462">WINBIO_BIR_HEADER</a>
 

 

