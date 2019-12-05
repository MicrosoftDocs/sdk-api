---
UID: NE:fsrmenums._FsrmCommitOptions
title: FsrmCommitOptions (fsrmenums.h)
description: Defines the options for committing a collection of objects.
old-location: fsrm\fsrmcommitoptions.htm
tech.root: fsrm
ms.assetid: eb362bd8-c11f-404e-be54-0e16007494a7
ms.date: 12/05/2018
ms.keywords: FsrmCommitOptions, FsrmCommitOptions enumeration [File Server Resource Manager], FsrmCommitOptions_Asynchronous, FsrmCommitOptions_None, fs.fsrmcommitoptions, fsrm.fsrmcommitoptions, fsrmenums/FsrmCommitOptions, fsrmenums/FsrmCommitOptions_Asynchronous, fsrmenums/FsrmCommitOptions_None
ms.topic: enum
f1_keywords:
- fsrmenums/FsrmCommitOptions
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
- FsrmCommitOptions
targetos: Windows
req.typenames: FsrmCommitOptions
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">IFsrmFileScreenTemplate::CommitAndUpdateDerived</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-commitandupdatederived">IFsrmQuotaTemplate::CommitAndUpdateDerived</a>
 

 

