---
UID: NE:fsrmenums._FsrmTemplateApplyOptions
title: FsrmTemplateApplyOptions (fsrmenums.h)
author: windows-sdk-content
description: Defines the options for applying template changes to derived objects.
old-location: fsrm\fsrmtemplateapplyoptions.htm
tech.root: fsrm
ms.assetid: 44a8e280-4005-476c-a43d-184c18825129
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmTemplateApplyOptions, FsrmTemplateApplyOptions enumeration [File Server Resource Manager], FsrmTemplateApplyOptions_ApplyToDerivedAll, FsrmTemplateApplyOptions_ApplyToDerivedMatching, fs.fsrmtemplateapplyoptions, fsrm.fsrmtemplateapplyoptions, fsrmenums/FsrmTemplateApplyOptions, fsrmenums/FsrmTemplateApplyOptions_ApplyToDerivedAll, fsrmenums/FsrmTemplateApplyOptions_ApplyToDerivedMatching
ms.topic: enum
f1_keywords: 
 - "fsrmenums/FsrmTemplateApplyOptions"
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
 - FsrmTemplateApplyOptions
targetos: Windows
req.typenames: FsrmTemplateApplyOptions
req.redist: 
ms.custom: 19H1
---

# FsrmTemplateApplyOptions enumeration


## -description


Defines the options for applying template changes to derived objects.


## -enum-fields




### -field FsrmTemplateApplyOptions_ApplyToDerivedMatching

Apply template changes to derived objects only if the object's properties match the template's properties.

Note that the comparison is made against the template as it exists in the database, not your local copy that 
       has not been committed yet.


### -field FsrmTemplateApplyOptions_ApplyToDerivedAll

Apply template changes to all derived objects, whether their properties match the template's or not.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">IFsrmFileScreenTemplate::CommitAndUpdateDerived</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-commitandupdatederived">IFsrmQuotaTemplate::CommitAndUpdateDerived</a>
 

 

