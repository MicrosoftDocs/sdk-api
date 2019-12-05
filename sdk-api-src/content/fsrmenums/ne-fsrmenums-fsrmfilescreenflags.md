---
UID: NE:fsrmenums._FsrmFileScreenFlags
title: FsrmFileScreenFlags (fsrmenums.h)
description: Defines the options for failing IO operations that violate a file screen.
old-location: fsrm\fsrmfilescreenflags.htm
tech.root: fsrm
ms.assetid: 5f0029e5-fe0a-453e-b226-6d4f31f650c5
ms.date: 12/05/2018
ms.keywords: FsrmFileScreenFlags, FsrmFileScreenFlags enumeration [File Server Resource Manager], FsrmFileScreenFlags_Enforce, fs.fsrmfilescreenflags, fsrm.fsrmfilescreenflags, fsrmenums/FsrmFileScreenFlags, fsrmenums/FsrmFileScreenFlags_Enforce
ms.topic: enum
f1_keywords:
- fsrmenums/FsrmFileScreenFlags
dev_langs:
- c++
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
- FsrmFileScreenFlags
targetos: Windows
req.typenames: FsrmFileScreenFlags
req.redist: 
ms.custom: 19H1
---

# FsrmFileScreenFlags enumeration


## -description


Defines the options for failing IO operations that violate a file screen.


## -enum-fields




### -field FsrmFileScreenFlags_Enforce

If this flag is set, the server will fail any IO operation that violates the file screen. If this flag is 
      not set, the server will not fail violating IO operations but will still run any action associated with the file 
      screen.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-get_filescreenflags">IFsrmFileScreenBase::FileScreenFlags</a>
 

 

