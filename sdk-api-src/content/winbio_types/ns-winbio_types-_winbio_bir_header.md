---
UID: NS:winbio_types._WINBIO_BIR_HEADER
title: "_WINBIO_BIR_HEADER"
author: windows-driver-content
description: Contains the header of a biometric information record (BIR).
old-location: secbiomet\winbio_bir_header.htm
old-project: SecBioMet
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_BIR_HEADER, WINBIO_BIR_HEADER, WINBIO_BIR_HEADER structure [Windows Biometric Framework API], WINBIO_DATA_FLAG_INTEGRITY, WINBIO_DATA_FLAG_INTERMEDIATE, WINBIO_DATA_FLAG_OPTION_MASK_PRESENT, WINBIO_DATA_FLAG_PRIVACY, WINBIO_DATA_FLAG_PROCESSED, WINBIO_DATA_FLAG_RAW, WINBIO_DATA_FLAG_SIGNED, WINBIO_DATA_QUALITY_NOT_SET, WINBIO_DATA_QUALITY_NOT_SUPPORTED, WINBIO_NO_FORMAT_OWNER_AVAILABLE, WINBIO_NO_FORMAT_TYPE_AVAILABLE, _WINBIO_BIR_HEADER, secbiomet.winbio_bir_header, winbio_types/WINBIO_BIR_HEADER"
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
req.typenames: WINBIO_BIR_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_BIR_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_BIR_HEADER structure


## -description


The <b>WINBIO_BIR_HEADER</b> structure contains the header of a biometric information record (BIR).


## -struct-fields




### -field ValidityPeriod

The  period for which the BIR is valid.



#### BeginDate

The date and time, in Coordinated Universal Time, that the validity period starts.



#### EndDate

The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.


### -field ValidFields

Bitmask that specifies which fields in this structure are valid. For more information, see <a href="https://msdn.microsoft.com/D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1">WINBIO_BIR_FIELD Constants</a>.


### -field HeaderVersion

A <b>WINBIO_BIR_VERSION</b> constant that specifies the header version. Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number. Currently this must be  WINBIO_CBEFF_HEADER_VERSION (0x11).


### -field PatronHeaderVersion

A <b>WINBIO_BIR_VERSION</b> constant that specifies the header version. Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number. Currently this must be  WINBIO_PATRON_HEADER_VERSION (0x11).


### -field DataFlags

A value that specifies the format of the header data. This can be a bitwise <b>OR</b> of the following security and processing level flags. For more information, see <a href="https://msdn.microsoft.com/F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C">WINBIO_BIR_DATA_FLAGS Constants</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_PRIVACY"></a><a id="winbio_data_flag_privacy"></a><dl>
<dt><b>WINBIO_DATA_FLAG_PRIVACY</b></dt>
<dt>((UCHAR)0x02)</dt>
</dl>
</td>
<td width="60%">
The data is encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_INTEGRITY"></a><a id="winbio_data_flag_integrity"></a><dl>
<dt><b>WINBIO_DATA_FLAG_INTEGRITY</b></dt>
<dt>((UCHAR)0x01)</dt>
</dl>
</td>
<td width="60%">
The data is digitally signed or protected by a message authentication code (MAC).

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_SIGNED"></a><a id="winbio_data_flag_signed"></a><dl>
<dt><b>WINBIO_DATA_FLAG_SIGNED</b></dt>
<dt>((UCHAR)0x04)</dt>
</dl>
</td>
<td width="60%">
If this flag and the <b>WINBIO_DATA_FLAG_INTEGRITY</b> flag are set, the data is signed. If this flag is not set but the <b>WINBIO_DATA_FLAG_INTEGRITY</b> flag is set, a MAC is computed over the data.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_RAW"></a><a id="winbio_data_flag_raw"></a><dl>
<dt><b>WINBIO_DATA_FLAG_RAW</b></dt>
<dt>((UCHAR)0x20)</dt>
</dl>
</td>
<td width="60%">
The data is in the format with which it was captured.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_INTERMEDIATE"></a><a id="winbio_data_flag_intermediate"></a><dl>
<dt><b>WINBIO_DATA_FLAG_INTERMEDIATE</b></dt>
<dt>((UCHAR)0x40)</dt>
</dl>
</td>
<td width="60%">
The data is not raw but has not been completely processed.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_PROCESSED"></a><a id="winbio_data_flag_processed"></a><dl>
<dt><b>WINBIO_DATA_FLAG_PROCESSED</b></dt>
<dt>((UCHAR)0x80)</dt>
</dl>
</td>
<td width="60%">
The data has been processed.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></a><a id="winbio_data_flag_option_mask_present"></a><dl>
<dt><b>WINBIO_DATA_FLAG_OPTION_MASK_PRESENT</b></dt>
<dt>((UCHAR)0x08)</dt>
</dl>
</td>
<td width="60%">
This value is always 1.

</td>
</tr>
</table>
 


### -field Type

A WINBIO_BIOMETRIC_TYPE value that specifies the type of biometric data referenced in the biometric information record. Currently only <b>WINBIO_TYPE_FINGERPRINT</b> is supported. For more information, see <a href="https://msdn.microsoft.com/DCBDB5F9-FF81-44C1-B439-2B8C02483212">WINBIO_BIOMETRIC_TYPE Constants</a>.


### -field Subtype

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the sub-factor associated with the biometric data. For more information, see Remarks and <a href="https://msdn.microsoft.com/019569A9-6184-4E75-9B82-C98F4F45F61A">WINBIO_BIOMETRIC_SUBTYPE Constants</a>.


### -field Purpose

A <b>WINBIO_BIR_PURPOSE</b> mask that specifies the intended use of the data.  This can be a bitwise <b>OR</b> of the following values. For more information, see <a href="https://msdn.microsoft.com/AAFD3203-4D3D-43B5-A833-1258E1E281D3">WINBIO_BIR_PURPOSE Constants</a>.<ul>
<li>WINBIO_PURPOSE_VERIFY</li>
<li>WINBIO_PURPOSE_IDENTIFY</li>
<li>WINBIO_PURPOSE_ENROLL</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION</li>
<li>WINBIO_PURPOSE_AUDIT</li>
</ul>



### -field DataQuality

A value that specifies the relative quality of the biometric data in the biometric information record (BIR). This can be an integer from 0 to 100 or one of the following values. For more information, see <a href="https://msdn.microsoft.com/A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C">WINBIO_BIR_QUALITY Constants</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_QUALITY_NOT_SET"></a><a id="winbio_data_quality_not_set"></a><dl>
<dt><b>WINBIO_DATA_QUALITY_NOT_SET</b></dt>
<dt>((WINBIO_BIR_QUALITY)-1)</dt>
</dl>
</td>
<td width="60%">
Quality measurements are supported by the BIR creator but no value is set in the BIR.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></a><a id="winbio_data_quality_not_supported"></a><dl>
<dt><b>WINBIO_DATA_QUALITY_NOT_SUPPORTED</b></dt>
<dt>((WINBIO_BIR_QUALITY)-2)</dt>
</dl>
</td>
<td width="60%">
Quality measurements are not supported by the BIR creator.

</td>
</tr>
</table>
 


### -field CreationDate

The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.


### -field BiometricDataFormat

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536473">WINBIO_REGISTERED_FORMAT</a> structure that specifies the data format of the standard data block in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a> structure. The <b>WINBIO_REGISTERED_FORMAT</b> members cannot be zero. You can use the following constants to simplify error checking.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></a><a id="winbio_no_format_owner_available"></a><dl>
<dt><b>WINBIO_NO_FORMAT_OWNER_AVAILABLE</b></dt>
<dt>((USHORT)0)</dt>
</dl>
</td>
<td width="60%">
No IBIA (International Biometric Industry Association) assigned owner value has been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></a><a id="winbio_no_format_type_available"></a><dl>
<dt><b>WINBIO_NO_FORMAT_TYPE_AVAILABLE</b></dt>
<dt>((USHORT)0)</dt>
</dl>
</td>
<td width="60%">
No format type has been specified.

</td>
</tr>
</table>
 


### -field ProductId

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff536473">WINBIO_REGISTERED_FORMAT</a> structure that specifies the product ID of the component that generated the standard data block in the BIR.  The <b>WINBIO_REGISTERED_FORMAT</b> members can be zero.


## -remarks



The <i>Subtype</i> parameter specifies the sub-factor associated with the biometric data. Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:

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
<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>Subtype</i> parameter value. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>
If any of the following bits are asserted, the <b>WINBIO_BIR_HEADER</b> structure is not correctly formed.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/019569A9-6184-4E75-9B82-C98F4F45F61A">WINBIO_BIOMETRIC_SUBTYPE Constants</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a>



<a href="https://msdn.microsoft.com/F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C">WINBIO_BIR_DATA_FLAGS Constants</a>



<a href="https://msdn.microsoft.com/D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1">WINBIO_BIR_FIELD Constants</a>



<a href="https://msdn.microsoft.com/AAFD3203-4D3D-43B5-A833-1258E1E281D3">WINBIO_BIR_PURPOSE Constants</a>



<a href="https://msdn.microsoft.com/A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C">WINBIO_BIR_QUALITY Constants</a>



<a href="https://msdn.microsoft.com/FBB8AE77-0FA2-46DE-B2F4-55D17CB6E7AB">WINBIO_BIR_VERSION Constants</a>
 

 

