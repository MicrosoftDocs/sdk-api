---
UID: NE:fsrmenums._FsrmFileStreamingMode
title: FsrmFileStreamingMode (fsrmenums.h)
description: Defines the streaming modes to use for the file stream.
helpviewer_keywords: ["FsrmFileStreamingMode","FsrmFileStreamingMode enumeration [File Server Resource Manager]","FsrmFileStreamingMode_Read","FsrmFileStreamingMode_Unknown","FsrmFileStreamingMode_Write","fs.fsrmfilestreamingmode","fsrm.fsrmfilestreamingmode","fsrmenums/FsrmFileStreamingMode","fsrmenums/FsrmFileStreamingMode_Read","fsrmenums/FsrmFileStreamingMode_Unknown","fsrmenums/FsrmFileStreamingMode_Write"]
old-location: fsrm\fsrmfilestreamingmode.htm
tech.root: fsrm
ms.assetid: a2f7de78-7102-43f9-a7b8-b35ac0b7286a
ms.date: 12/05/2018
ms.keywords: FsrmFileStreamingMode, FsrmFileStreamingMode enumeration [File Server Resource Manager], FsrmFileStreamingMode_Read, FsrmFileStreamingMode_Unknown, FsrmFileStreamingMode_Write, fs.fsrmfilestreamingmode, fsrm.fsrmfilestreamingmode, fsrmenums/FsrmFileStreamingMode, fsrmenums/FsrmFileStreamingMode_Read, fsrmenums/FsrmFileStreamingMode_Unknown, fsrmenums/FsrmFileStreamingMode_Write
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: FsrmFileStreamingMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmFileStreamingMode
 - fsrmenums/_FsrmFileStreamingMode
 - FsrmFileStreamingMode
 - fsrmenums/FsrmFileStreamingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileStreamingMode
---

# FsrmFileStreamingMode enumeration


## -description

Defines the streaming modes to use for the file stream.

## -enum-fields

### -field FsrmFileStreamingMode_Unknown:0

The streaming mode is unknown; do not use this value.

### -field FsrmFileStreamingMode_Read:0x1

Use the streaming interface for reading from the file.

### -field FsrmFileStreamingMode_Write:0x2

Use the streaming interface for writing to the  file.

## -see-also

<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmfilestreamingmode">FsrmFileStreamingMode</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-getfilestreaminterface">IFsrmPropertyBag::GetFileStreamInterface</a>
