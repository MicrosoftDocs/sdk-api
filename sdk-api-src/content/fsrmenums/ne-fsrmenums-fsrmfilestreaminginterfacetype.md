---
UID: NE:fsrmenums._FsrmFileStreamingInterfaceType
title: FsrmFileStreamingInterfaceType (fsrmenums.h)
description: Defines the possible streaming interface types.
helpviewer_keywords: ["FsrmFileStreamingInterfaceType","FsrmFileStreamingInterfaceType enumeration [File Server Resource Manager]","FsrmFileStreamingInterfaceType_ILockBytes","FsrmFileStreamingInterfaceType_IStream","FsrmFileStreamingInterfaceType_Unknown","fs.fsrmfilestreaminginterfacetype","fsrm.fsrmfilestreaminginterfacetype","fsrmenums/FsrmFileStreamingInterfaceType","fsrmenums/FsrmFileStreamingInterfaceType_ILockBytes","fsrmenums/FsrmFileStreamingInterfaceType_IStream","fsrmenums/FsrmFileStreamingInterfaceType_Unknown"]
old-location: fsrm\fsrmfilestreaminginterfacetype.htm
tech.root: fsrm
ms.assetid: 182dde15-f8d6-42ab-a9d2-85f0a0a4d670
ms.date: 12/05/2018
ms.keywords: FsrmFileStreamingInterfaceType, FsrmFileStreamingInterfaceType enumeration [File Server Resource Manager], FsrmFileStreamingInterfaceType_ILockBytes, FsrmFileStreamingInterfaceType_IStream, FsrmFileStreamingInterfaceType_Unknown, fs.fsrmfilestreaminginterfacetype, fsrm.fsrmfilestreaminginterfacetype, fsrmenums/FsrmFileStreamingInterfaceType, fsrmenums/FsrmFileStreamingInterfaceType_ILockBytes, fsrmenums/FsrmFileStreamingInterfaceType_IStream, fsrmenums/FsrmFileStreamingInterfaceType_Unknown
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
req.typenames: FsrmFileStreamingInterfaceType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmFileStreamingInterfaceType
 - fsrmenums/_FsrmFileStreamingInterfaceType
 - FsrmFileStreamingInterfaceType
 - fsrmenums/FsrmFileStreamingInterfaceType
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
 - FsrmFileStreamingInterfaceType
---

# FsrmFileStreamingInterfaceType enumeration


## -description

Defines the possible streaming interface types.

## -enum-fields

### -field FsrmFileStreamingInterfaceType_Unknown:0

The streaming interface type is unknown; do not use this value.

### -field FsrmFileStreamingInterfaceType_ILockBytes:0x1

Use an <a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> interface to stream the file.

### -field FsrmFileStreamingInterfaceType_IStream:0x2

Use an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface to stream the file.

## -see-also

<a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmfilestreamingmode">FsrmFileStreamingMode</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmpropertybag-getfilestreaminterface">IFsrmPropertyBag::GetFileStreamInterface</a>
