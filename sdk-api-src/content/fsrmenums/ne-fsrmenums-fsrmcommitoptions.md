---
UID: NE:fsrmenums._FsrmCommitOptions
title: FsrmCommitOptions (fsrmenums.h)
author: windows-sdk-content
description: Defines the options for committing a collection of objects.
old-location: fsrm\fsrmcommitoptions.htm
tech.root: fsrm
ms.assetid: eb362bd8-c11f-404e-be54-0e16007494a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmCommitOptions, FsrmCommitOptions enumeration [File Server Resource Manager], FsrmCommitOptions_Asynchronous, FsrmCommitOptions_None, fs.fsrmcommitoptions, fsrm.fsrmcommitoptions, fsrmenums/FsrmCommitOptions, fsrmenums/FsrmCommitOptions_Asynchronous, fsrmenums/FsrmCommitOptions_None
ms.topic: enum
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
 - FsrmCommitOptions
product: Windows
targetos: Windows
req.typenames: FsrmCommitOptions
req.redist: 
---

# FsrmCommitOptions enumeration


## -description


Defines the options for committing a collection of objects.


## -enum-fields




### -field FsrmCommitOptions_None

Use no options and commit the collection of objects synchronously.


### -field FsrmCommitOptions_Asynchronous

Reserved. Do not use.


## -remarks



The <b>FsrmCommitOptions_Asynchronous</b> option is not supported.




## -see-also




<a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a>



<a href="https://msdn.microsoft.com/6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7">IFsrmFileScreenTemplate::CommitAndUpdateDerived</a>



<a href="https://msdn.microsoft.com/fecb034f-3f11-4d37-9468-56d4ea6268e7">IFsrmQuotaTemplate::CommitAndUpdateDerived</a>
 

 

