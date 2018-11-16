---
UID: NE:fsrmenums._FsrmFileStreamingInterfaceType
title: "_FsrmFileStreamingInterfaceType"
author: windows-sdk-content
description: Defines the possible streaming interface types.
old-location: fsrm\fsrmfilestreaminginterfacetype.htm
tech.root: Fsrm
ms.assetid: 182dde15-f8d6-42ab-a9d2-85f0a0a4d670
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FsrmFileStreamingInterfaceType, FsrmFileStreamingInterfaceType enumeration [File Server Resource Manager], FsrmFileStreamingInterfaceType_ILockBytes, FsrmFileStreamingInterfaceType_IStream, FsrmFileStreamingInterfaceType_Unknown, _FsrmFileStreamingInterfaceType, fs.fsrmfilestreaminginterfacetype, fsrm.fsrmfilestreaminginterfacetype, fsrmenums/FsrmFileStreamingInterfaceType, fsrmenums/FsrmFileStreamingInterfaceType_ILockBytes, fsrmenums/FsrmFileStreamingInterfaceType_IStream, fsrmenums/FsrmFileStreamingInterfaceType_Unknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileStreamingInterfaceType
product: Windows
targetos: Windows
req.typenames: FsrmFileStreamingInterfaceType
req.redist: 
---

# _FsrmFileStreamingInterfaceType enumeration


## -description


Defines the possible streaming interface types.


## -enum-fields




### -field FsrmFileStreamingInterfaceType_Unknown

The streaming interface type is unknown; do not use this value.


### -field FsrmFileStreamingInterfaceType_ILockBytes

Use an <a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface to stream the file.


### -field FsrmFileStreamingInterfaceType_IStream

Use an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to stream the file.


## -see-also




<a href="https://msdn.microsoft.com/a2f7de78-7102-43f9-a7b8-b35ac0b7286a">FsrmFileStreamingMode</a>



<a href="https://msdn.microsoft.com/e5250f0f-c8b4-4579-a4c2-b4f6ee48acdc">IFsrmPropertyBag::GetFileStreamInterface</a>
 

 

