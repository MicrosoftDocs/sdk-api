---
UID: NE:vds._VDS_DRIVE_LETTER_FLAG
title: "_VDS_DRIVE_LETTER_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for a drive letter.
old-location: base\vds_drive_letter_flag.htm
old-project: vds
ms.assetid: f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_DLF_NON_PERSISTENT, VDS_DRIVE_LETTER_FLAG, VDS_DRIVE_LETTER_FLAG enumeration [VDS], _VDS_DRIVE_LETTER_FLAG, base.vds_drive_letter_flag, vds/VDS_DLF_NON_PERSISTENT, vds/VDS_DRIVE_LETTER_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
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
tech.root: 
req.typenames: VDS_DRIVE_LETTER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_DRIVE_LETTER_FLAG
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_DRIVE_LETTER_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a drive letter.


## -enum-fields




### -field VDS_DLF_NON_PERSISTENT

If set, the drive letter disappears after the computer reboots.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/b944e29a-85b0-4cab-b804-1a09a19caddb">VDS_DRIVE_LETTER_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DRIVE_LETTER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DRIVE_LETTER_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

