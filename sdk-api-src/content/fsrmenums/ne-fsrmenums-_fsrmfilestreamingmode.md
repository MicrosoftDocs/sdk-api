---
UID: NE:fsrmenums._FsrmFileStreamingMode
title: "_FsrmFileStreamingMode"
author: windows-sdk-content
description: Defines the streaming modes to use for the file stream.
old-location: fsrm\fsrmfilestreamingmode.htm
old-project: fsrm
ms.assetid: a2f7de78-7102-43f9-a7b8-b35ac0b7286a
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmFileStreamingMode, FsrmFileStreamingMode enumeration [File Server Resource Manager], FsrmFileStreamingMode_Read, FsrmFileStreamingMode_Unknown, FsrmFileStreamingMode_Write, _FsrmFileStreamingMode, fs.fsrmfilestreamingmode, fsrm.fsrmfilestreamingmode, fsrmenums/FsrmFileStreamingMode, fsrmenums/FsrmFileStreamingMode_Read, fsrmenums/FsrmFileStreamingMode_Unknown, fsrmenums/FsrmFileStreamingMode_Write
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmEnums.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmFileStreamingMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileStreamingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmFileStreamingMode enumeration


## -description


Defines the streaming modes to use for the file stream.


## -enum-fields




### -field FsrmFileStreamingMode_Unknown

The streaming mode is unknown; do not use this value.


### -field FsrmFileStreamingMode_Read

Use the streaming interface for reading from the file.


### -field FsrmFileStreamingMode_Write

Use the streaming interface for writing to the  file.


## -see-also




<a href="https://msdn.microsoft.com/a2f7de78-7102-43f9-a7b8-b35ac0b7286a">FsrmFileStreamingMode</a>



<a href="https://msdn.microsoft.com/e5250f0f-c8b4-4579-a4c2-b4f6ee48acdc">IFsrmPropertyBag::GetFileStreamInterface</a>
 

 

