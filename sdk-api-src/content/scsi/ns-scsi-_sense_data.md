---
UID: NS:scsi._SENSE_DATA
title: "_SENSE_DATA"
author: windows-driver-content
description: Used to report status or error information in response to a SCSI Request Sense command.
old-location: winprog\sense_data.htm
old-project: DevNotes
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PFIXED_SENSE_DATA, *PSENSE_DATA, Aborted Command, Data Protect, Equal, FIXED_SENSE_DATA, Firmware Error, Hardware Error, Illegal Request, Medium Error, Miscompare, No Sense, Not Ready, PSENSE_DATA, PSENSE_DATA structure pointer [Windows API], Recovered Error, SENSE_DATA, SENSE_DATA structure [Windows API], Unit Attention, Volume Overflow, _SENSE_DATA, scsi/PSENSE_DATA, scsi/SENSE_DATA, winprog.sense_data"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: scsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SENSE_DATA, *PSENSE_DATA, FIXED_SENSE_DATA, *PFIXED_SENSE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Scsi.h
api_name:
-	SENSE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SENSE_DATA structure


## -description


Used to report status or error information in response to a SCSI 
    <b>Request Sense</b> command.


## -struct-fields




### -field ErrorCode

The report type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x70</dt>
</dl>
</td>
<td width="60%">
Current errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x71</dt>
</dl>
</td>
<td width="60%">
Deferred errors.

</td>
</tr>
</table>
 


### -field Valid

1 if the <b>Information</b> field is defined in a standard; otherwise the 
      <b>Information</b> field is vendor-specific and not defined by a standard.


### -field SegmentNumber

Obsolete.


### -field SenseKey

Indicates the category of error. 



#### No Sense (0x0)



#### Recovered Error (0x1)



#### Not Ready (0x2)



#### Medium Error (0x3)



#### Hardware Error (0x4)



#### Illegal Request (0x5)



#### Unit Attention (0x6)



#### Data Protect (0x7)



#### Firmware Error (0x9)



#### Aborted Command (0xB)



#### Equal (0xC)



#### Volume Overflow (0xD)



#### Miscompare (0xE)


### -field Reserved

Reserved.


### -field IncorrectLength

1 if the requested logical block length does not match the logical block length of the data on the media.


### -field EndOfMedia

1 if a sequential-access device has reached end-of-media, or a printer is out of paper. 


### -field FileMark

1 if the current command has reached a filemark or setmark. Only valid for sequential-access devices.


### -field Information

Device-type or command specific data.


### -field AdditionalSenseLength

The length in bytes of the remainder of the structure. The total length minus 7.


### -field CommandSpecificInformation

Command-specific data. Values are defined in the appropriate command standard.


### -field AdditionalSenseCode

Device specific code that describes the error reported in the <b>SenseKey</b> field.


### -field AdditionalSenseCodeQualifier

Can contain additional detail about the <b>AdditionalSenseCode</b> field.


### -field FieldReplaceableUnitCode

Vender-specific information about the component associated with this sense data.


### -field SenseKeySpecific

The content and format of the sense key specific information is determined by the value of the 
      <b>SenseKey</b> field.


## -remarks



For more information about the sense data format, see 
    <a href="http://en.wikipedia.org/wiki/SCSI_Request_Sense_Command">SCSI Request Sense Command</a> 
    (http://en.wikipedia.org/wiki/SCSI_Request_Sense_Command).




## -see-also




<a href="https://msdn.microsoft.com/BA7056D1-0FD6-4769-BCFB-59335A96C503">SCSI_PASS_THROUGH_DIRECT_WITH_AUXILIARY</a>



<a href="https://msdn.microsoft.com/5ADD3595-4582-4D49-9F77-F863370A225C">iSCSI Target Pass-Through</a>
 

 

