---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0016
title: DSMCC_FILTER_OPTIONS (mpeg2structs.h)
description: The DSMCC_FILTER_OPTIONS structure specifies additional filtering criteria for the DSM-CC portions of the section header.
helpviewer_keywords: ["DSMCC_FILTER_OPTIONS","DSMCC_FILTER_OPTIONS structure [Microsoft TV Technologies]","mpeg2structs/DSMCC_FILTER_OPTIONS","mstv.dsmcc_filter_options"]
old-location: mstv\dsmcc_filter_options.htm
tech.root: mstv
ms.assetid: a8be6d69-1b41-49f0-8588-624b8de98678
ms.date: 12/05/2018
ms.keywords: DSMCC_FILTER_OPTIONS, DSMCC_FILTER_OPTIONS structure [Microsoft TV Technologies], mpeg2structs/DSMCC_FILTER_OPTIONS, mstv.dsmcc_filter_options
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSMCC_FILTER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0016
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0016
 - DSMCC_FILTER_OPTIONS
 - mpeg2structs/DSMCC_FILTER_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - DSMCC_FILTER_OPTIONS
---

# DSMCC_FILTER_OPTIONS structure


## -description

The <b>DSMCC_FILTER_OPTIONS</b> structure specifies additional filtering criteria for the DSM-CC portions of the section header.

## -struct-fields

### -field fSpecifyProtocol

If this flag is <b>TRUE</b>, the protocolDiscriminator field in the header must match the value of the <b>Protocol</b> structure member. Otherwise, the protocolDiscriminator field is ignored.

### -field Protocol

Specifies a value for the protocolDiscriminator field. For MPEG-2 DSM-CC messages, this field must equal 0x11.

### -field fSpecifyType

If this field is <b>TRUE</b>, the dsmccType field in the header must match the value of the <b>Type</b> structure member. Otherwise, the dsmccType field is ignored.

### -field Type

Specifies a value for the dsmccType field, which defines the DSM-CC message type.

### -field fSpecifyMessageId

If this flag is <b>TRUE</b>, the messageId field in the header must match the value of the <b>MessageId</b> structure member. Otherwise, the messageId field is ignored.

### -field MessageId

Specifies a value for the messageId field, which defines the DSM-CC message within the scope of the message type.

### -field fSpecifyTransactionId

If this flag is <b>TRUE</b>, the transactionId (or downloadId) field in the header must match the value of the <b>TransactionId</b> structure member. Otherwise, the transactionId/downloadId field is ignored.

### -field fUseTrxIdMessageIdMask

If this flag is <b>TRUE</b>, the transactionId bits are masked so that the following subfields are ignored:

<ul>
<li>Updated flag</li>
<li>Version </li>
</ul>
The following subfields are matched against the <b>TransactionId</b> structure member:

<ul>
<li>Identification</li>
<li>Originator</li>
</ul>
For more information about the subfields within the transactionId, see section 4.6.5 of TR 101 202, <i>Digital Video Broadcasting (DVB); Implementation Guidelines for Data Broadcasting</i>. (This resource may not be available in some languages 

and countries.)

This flag is ignored if <b>fSpecifyTransactionId</b> is <b>FALSE</b>.

### -field TransactionId

Specifies a value for the transactionId field.

### -field fSpecifyModuleVersion

If this flag is <b>TRUE</b>, the moduleVersion field in the header must match the value of the <b>ModuleVersion</b> structure member. Otherwise, the moduleVersion field is ignored.

### -field ModuleVersion

Specifies a value for the moduleVersion field.

### -field fSpecifyBlockNumber

If this flag is <b>TRUE</b>, the blockNumber field in the header must match the value of the BlockNumber structure member. Otherwise, the moduleVersion field is ignored.

### -field BlockNumber

Specifies a value for the blockNumber field.

### -field fGetModuleCall

If this flag is <b>TRUE</b>, the <b>NumberOfBlocksInModule</b> structure member specifies the number of blocks in the module. Applies only to download data block (DDB) messages.

### -field NumberOfBlocksInModule

Specifies the number of blocks in the module. Applies only to DDB messages.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>



<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER Structure</a>