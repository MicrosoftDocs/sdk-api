---
UID: NS:winbio_ioctl._WINBIO_CAPTURE_PARAMETERS
title: "_WINBIO_CAPTURE_PARAMETERS"
author: windows-driver-content
description: The IOCTL_BIOMETRIC_CAPTURE_DATA IOCTL uses the WINBIO_CAPTURE_PARAMETERS structure as input.
old-location: biometric\winbio_capture_parameters.htm
old-project: biometric
ms.assetid: 60f35000-c62d-4d1b-8592-862c2d74b7a2
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: "*PWINBIO_CAPTURE_PARAMETERS, PWINBIO_CAPTURE_PARAMETERS, PWINBIO_CAPTURE_PARAMETERS structure pointer [Biometric Devices], WINBIO_CAPTURE_PARAMETERS, WINBIO_CAPTURE_PARAMETERS structure [Biometric Devices], _WINBIO_CAPTURE_PARAMETERS, biometric.winbio_capture_parameters, biometric_ref_fbd581b2-ced0-4c0d-b76c-be5a469252fd.xml, winbio_ioctl/PWINBIO_CAPTURE_PARAMETERS, winbio_ioctl/WINBIO_CAPTURE_PARAMETERS"
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
req.typenames: WINBIO_CAPTURE_PARAMETERS, *PWINBIO_CAPTURE_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_ioctl.h
api_name:
-	WINBIO_CAPTURE_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_CAPTURE_PARAMETERS structure


## -description


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff536429">IOCTL_BIOMETRIC_CAPTURE_DATA</a> IOCTL uses the WINBIO_CAPTURE_PARAMETERS structure as input.


## -struct-fields




### -field PayloadSize

The total size of the payload.


### -field Purpose

A WINBIO_BIR_PURPOSE purpose, that specifies how captured data is to be used, and as a result, how it should be optimized.  Some sensors will go into a different mode depending on the reason for the data capture.

The following code example shows the possible bitmask values for WINBIO_BIR_PURPOSE:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define WINBIO_NO_PURPOSE_AVAILABLE                     ((WINBIO_BIR_PURPOSE)0x00)
#define WINBIO_PURPOSE_VERIFY                           ((WINBIO_BIR_PURPOSE)0x01)
#define WINBIO_PURPOSE_IDENTIFY                         ((WINBIO_BIR_PURPOSE)0x02)
#define WINBIO_PURPOSE_ENROLL                           ((WINBIO_BIR_PURPOSE)0x04)
#define WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION          ((WINBIO_BIR_PURPOSE)0x08)
#define WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION        ((WINBIO_BIR_PURPOSE)0x10)
#define WINBIO_PURPOSE_AUDIT                            ((WINBIO_BIR_PURPOSE)0x80)</pre>
</td>
</tr>
</table></span></div>

### -field Format

Specifies the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536473">WINBIO_REGISTERED_FORMAT</a> format of the data to be returned.


### -field VendorFormat

An optional WINBIO_UUID vendor GUID.  This indicates the preferred format of the vendor-specific data in the BIR.


### -field Flags

Specifies the WINBIO_BIR_DATA_FLAGS level of processing and other attributes for the data to be returned.  If format owner and type are the Windows standard, this must be WINBIO_DATA_FLAG_RAW.

The following code example shows the possible bitmask values for WINBIO_BIR_DATA_FLAGS:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define WINBIO_DATA_FLAG_PRIVACY                ((UCHAR)0x02)
#define WINBIO_DATA_FLAG_INTEGRITY              ((UCHAR)0x01)
#define WINBIO_DATA_FLAG_SIGNED                 ((UCHAR)0x04)

#define WINBIO_DATA_FLAG_RAW                    ((UCHAR)0x20)
#define WINBIO_DATA_FLAG_INTERMEDIATE           ((UCHAR)0x40)
#define WINBIO_DATA_FLAG_PROCESSED              ((UCHAR)0x80)

#define WINBIO_DATA_FLAG_OPTION_MASK_PRESENT    ((UCHAR)0x08)   // Always '1'.</pre>
</td>
</tr>
</table></span></div>

## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536429">IOCTL_BIOMETRIC_CAPTURE_DATA</a>
 

 

