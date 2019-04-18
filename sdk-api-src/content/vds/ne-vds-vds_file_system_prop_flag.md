---
UID: NE:vds._VDS_FILE_SYSTEM_PROP_FLAG
title: VDS_FILE_SYSTEM_PROP_FLAG (vds.h)
author: windows-sdk-content
description: Defines the details of file-system compression.
old-location: base\vds_file_system_prop_flag.htm
tech.root: VDS
ms.assetid: f2776ee9-4809-4f99-b464-80b5b53f8675
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_FILE_SYSTEM_PROP_FLAG, VDS_FILE_SYSTEM_PROP_FLAG enumeration [VDS], VDS_FPF_COMPRESSED, base.vds_file_system_prop_flag, vds/VDS_FILE_SYSTEM_PROP_FLAG, vds/VDS_FPF_COMPRESSED
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FILE_SYSTEM_PROP_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_PROP_FLAG
req.redist: 
ms.custom: 19H1
---

# VDS_FILE_SYSTEM_PROP_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of file-system compression.


## -enum-fields




### -field VDS_FPF_COMPRESSED

If set, the file system supports file compression.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_PROP_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_PROP_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a>
 

 

