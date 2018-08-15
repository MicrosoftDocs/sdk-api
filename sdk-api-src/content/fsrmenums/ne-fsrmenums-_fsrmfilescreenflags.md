---
UID: NE:fsrmenums._FsrmFileScreenFlags
title: "_FsrmFileScreenFlags"
author: windows-sdk-content
description: Defines the options for failing IO operations that violate a file screen.
old-location: fsrm\fsrmfilescreenflags.htm
old-project: fsrm
ms.assetid: 5f0029e5-fe0a-453e-b226-6d4f31f650c5
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmFileScreenFlags, FsrmFileScreenFlags enumeration [File Server Resource Manager], FsrmFileScreenFlags_Enforce, _FsrmFileScreenFlags, fs.fsrmfilescreenflags, fsrm.fsrmfilescreenflags, fsrmenums/FsrmFileScreenFlags, fsrmenums/FsrmFileScreenFlags_Enforce
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.typenames: FsrmFileScreenFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmFileScreenFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# _FsrmFileScreenFlags enumeration


## -description


Defines the options for failing IO operations that violate a file screen.


## -enum-fields




### -field FsrmFileScreenFlags_Enforce

If this flag is set, the server will fail any IO operation that violates the file screen. If this flag is 
      not set, the server will not fail violating IO operations but will still run any action associated with the file 
      screen.


## -see-also




<a href="https://msdn.microsoft.com/af888368-36a8-401e-b4df-6b0cc0dfb422">IFsrmFileScreenBase::FileScreenFlags</a>
 

 

