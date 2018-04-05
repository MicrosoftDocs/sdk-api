---
UID: NS:winbio_types._WINBIO_BDB_ANSI_381_RECORD
title: "_WINBIO_BDB_ANSI_381_RECORD"
author: windows-driver-content
description: Contains information about a single fingerprint or palm sample from an end user.
old-location: secbiomet\winbio_bdb_ansi_381_record.htm
old-project: SecBioMet
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BDB_ANSI_381_RECORD, WINBIO_BDB_ANSI_381_RECORD, WINBIO_BDB_ANSI_381_RECORD structure [Windows Biometric Framework API], _WINBIO_BDB_ANSI_381_RECORD, secbiomet.winbio_bdb_ansi_381_record, winbio_types/WINBIO_BDB_ANSI_381_RECORD"
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
req.typenames: WINBIO_BDB_ANSI_381_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BDB_ANSI_381_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BDB_ANSI_381_RECORD structure


## -description


The <b>WINBIO_BDB_ANSI_381_RECORD</b> structure contains information about a single fingerprint or palm sample from an end user. A collection of these structures is included in each <a href="https://msdn.microsoft.com/8b0caa50-9bba-45c4-b4bf-514540894793">WINBIO_BDB_ANSI_381_HEADER</a> structure.


## -struct-fields




### -field BlockLength

Contains the number of bytes in this structure plus the number of bytes of sample image data.


### -field HorizontalLineLength

Specifies the number of pixels in a horizontal line of the sample.


### -field VerticalLineLength

Specifies the number of pixels in a vertical line of the sample.


### -field Position

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the finger or palm used to generate the biometric sample. For more information, see Remarks.


### -field CountOfViews

This must be set to one (1);


### -field ViewNumber

This must be set to one (1);


### -field ImageQuality

Reserved. This must be 254 (0xFE).


### -field ImpressionType

Reserved.


### -field Reserved

Reserved. Must be set to zero (0).


## -remarks



The <i>Position</i> member specifies the area of the hand or palm used to make  the biometric sample. The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.

<ul>
<li>WINBIO_ANSI_381_POS_UNKNOWN</li>
<li>WINBIO_ANSI_381_POS_RH_THUMB</li>
<li>WINBIO_ANSI_381_POS_RH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_THUMB</li>
<li>WINBIO_ANSI_381_POS_LH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_LH_FOUR_FINGERS</li>
<li>WINBIO_ANSI_381_POS_TWO_THUMBS</li>
</ul>
<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>Position</i> value. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>
 

 

