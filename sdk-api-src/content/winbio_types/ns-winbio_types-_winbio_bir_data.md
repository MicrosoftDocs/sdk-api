---
UID: NS:winbio_types._WINBIO_BIR_DATA
title: "_WINBIO_BIR_DATA"
author: windows-driver-content
description: Specifies the size, in bytes, and the offset of a block of biometric information.
old-location: secbiomet\winbio_bir_data.htm
old-project: SecBioMet
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BIR_DATA, WINBIO_BIR_DATA, WINBIO_BIR_DATA structure [Windows Biometric Framework API], _WINBIO_BIR_DATA, secbiomet.winbio_bir_data, winbio_types/WINBIO_BIR_DATA"
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
req.typenames: WINBIO_BIR_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BIR_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BIR_DATA structure


## -description


The <b>WINBIO_BIR_DATA</b> structure specifies the size, in bytes, and the offset of a block of biometric information. This structure is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a> structure  to specify where the various parts of a biometric information record are located.


## -struct-fields




### -field Size

Size, in bytes, of the biometric information.


### -field Offset

Offset, in bytes from the beginning of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a> structure, of the biometric information.


## -remarks



The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.




## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536462">WINBIO_BIR_HEADER</a>
 

 

