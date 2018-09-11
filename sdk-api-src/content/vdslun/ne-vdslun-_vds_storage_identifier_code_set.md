---
UID: NE:vdslun._VDS_STORAGE_IDENTIFIER_CODE_SET
title: "_VDS_STORAGE_IDENTIFIER_CODE_SET"
author: windows-sdk-content
description: Defines the set of the valid code sets (encodings) of a storage identifier.
old-location: base\vds_storage_identifier_code_set.htm
tech.root: VDS
ms.assetid: 6b4a3282-dc0c-4974-8c4c-777a28fb9005
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VDSStorageIdCodeSetAscii, VDSStorageIdCodeSetBinary, VDSStorageIdCodeSetReserved, VDSStorageIdCodeSetUtf8, VDS_STORAGE_IDENTIFIER_CODE_SET, VDS_STORAGE_IDENTIFIER_CODE_SET enumeration [VDS], _VDS_STORAGE_IDENTIFIER_CODE_SET, base.vds_storage_identifier_code_set, vdslun/VDSStorageIdCodeSetAscii, vdslun/VDSStorageIdCodeSetBinary, vdslun/VDSStorageIdCodeSetReserved, vdslun/VDSStorageIdCodeSetUtf8, vdslun/VDS_STORAGE_IDENTIFIER_CODE_SET
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_IDENTIFIER_CODE_SET
product: Windows
targetos: Windows
req.typenames: VDS_STORAGE_IDENTIFIER_CODE_SET
req.redist: 
---

# _VDS_STORAGE_IDENTIFIER_CODE_SET enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of the valid code sets (encodings) of a storage identifier.


## -enum-fields




### -field VDSStorageIdCodeSetReserved

This value is reserved.


### -field VDSStorageIdCodeSetBinary

The storage identifier is encoded as binary data.


### -field VDSStorageIdCodeSetAscii

The storage identifier is encoded as ASCII data.


### -field VDSStorageIdCodeSetUtf8

The storage identifier is encoded as UTF-8.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.


## -remarks



The <a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a> structure includes 
    a <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> value as a member to indicate the code set of a storage identifier.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/8cc8b6d9-e189-44af-9f2b-2222b2eb0749">VDS_STORAGE_IDENTIFIER</a>
 

 

