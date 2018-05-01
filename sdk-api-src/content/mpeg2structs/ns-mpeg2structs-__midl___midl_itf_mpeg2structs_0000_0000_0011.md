---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0011
title: "__MIDL___MIDL_itf_mpeg2structs_0000_0000_0011"
author: windows-driver-content
description: The DSMCC_SECTION structure represents a DSM-CC section header. If a section contains a DSM-CC header, you can cast a SECTION pointer to a DSMCC_SECTION pointer. For more information, see the Remarks section in the SECTION reference.
old-location: mstv\dsmcc_section.htm
old-project: mstv
ms.assetid: b043f63c-cee0-4167-9b11-09b747f63b8d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: "*PDSMCC_SECTION, DSMCC_SECTION, DSMCC_SECTION structure [Microsoft TV Technologies], PDSMCC_SECTION, PDSMCC_SECTION structure pointer [Microsoft TV Technologies], __MIDL___MIDL_itf_mpeg2structs_0000_0000_0011, mpeg2structs/DSMCC_SECTION, mpeg2structs/PDSMCC_SECTION, mstv.dsmcc_section"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpeg2structs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: DSMCC_SECTION, *PDSMCC_SECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mpeg2Structs.h
api_name:
-	DSMCC_SECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0011 structure


## -description



The <b>DSMCC_SECTION</b> structure represents a DSM-CC section header. If a section contains a DSM-CC header, you can cast a <a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> pointer to a <b>DSMCC_SECTION</b> pointer. For more information, see the Remarks section in the <b>SECTION</b> reference.




## -struct-fields




### -field TableId

Specifies the table identifier (TID) of the section.


### -field Header

A union that contains the following members.



#### S

Contains packed header bits, as an <b>MPEG_HEADER_BITS_MIDL</b> structure. Applications should use the <b>Header.W</b> field instead.



#### W

Contains the header bits as a <b>WORD</b> type. To get the individual bitfields, coerce this member to an <a href="https://msdn.microsoft.com/e25d36af-ee72-4986-8d96-2bce8b19ac80">MPEG_HEADER_BITS</a> structure.


### -field TableIdExtension

Specifies the table_id_extension field.


### -field Version

A union that contains the following members.



#### S

Contains the version number and current/next indicator bit as an <b>MPEG_HEADER_VERSION_BITS_MIDL</b> structure. Applications should use the <b>Version.B</b> field instead.



#### B

Contains the version number and current/next indicator bit as a <b>BYTE</b> type. To get the individual bit fields, coerce this member to an <a href="https://msdn.microsoft.com/d9a33ca6-2e35-4f7c-8621-ce30effeb687">MPEG_HEADER_VERSION_BITS</a> structure.


### -field SectionNumber

Specifies the section_number field, which gives the section number for this section.


### -field LastSectionNumber

Specifies the last_section_number field, which gives the last (highest) section number for the table.


### -field ProtocolDiscriminator

Indicates that the message is an MPEG-2 DSM-CC message. The value of this field is always 0x11.


### -field DsmccType

Specifies the DSM-CC message type.


### -field MessageId

Specifies the DSM-CC message identifier.


### -field TransactionId

Specifies the transaction identifier.


### -field Reserved

Reserved bytes.


### -field AdaptationLength

Specifies the adaptation field length.


### -field MessageLength

Specifies the message length.


### -field RemainingData

Contains the remaining section data, as a byte array. The length of the array is <code>Header.W.SectionLength - 17</code> bytes.


## -remarks



This structure extends the <a href="https://msdn.microsoft.com/1403971f-5165-484c-9aa3-0cd489985545">LONG_SECTION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

