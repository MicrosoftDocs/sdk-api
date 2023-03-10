---
UID: NE:fsrmenums._FsrmEnumOptions
title: FsrmEnumOptions (fsrmenums.h)
description: Defines the options for enumerating collections of objects.
helpviewer_keywords: ["FsrmEnumOptions","FsrmEnumOptions enumeration [File Server Resource Manager]","FsrmEnumOptions_Asynchronous","FsrmEnumOptions_CheckRecycleBin","FsrmEnumOptions_IncludeClusterNodes","FsrmEnumOptions_IncludeDeprecatedObjects","FsrmEnumOptions_None","fs.fsrmenumoptions","fsrm.fsrmenumoptions","fsrmenums/FsrmEnumOptions","fsrmenums/FsrmEnumOptions_Asynchronous","fsrmenums/FsrmEnumOptions_CheckRecycleBin","fsrmenums/FsrmEnumOptions_IncludeClusterNodes","fsrmenums/FsrmEnumOptions_IncludeDeprecatedObjects","fsrmenums/FsrmEnumOptions_None"]
old-location: fsrm\fsrmenumoptions.htm
tech.root: fsrm
ms.assetid: 9c613d0c-c49a-4010-b66f-a63c57d693f7
ms.date: 12/05/2018
ms.keywords: FsrmEnumOptions, FsrmEnumOptions enumeration [File Server Resource Manager], FsrmEnumOptions_Asynchronous, FsrmEnumOptions_CheckRecycleBin, FsrmEnumOptions_IncludeClusterNodes, FsrmEnumOptions_IncludeDeprecatedObjects, FsrmEnumOptions_None, fs.fsrmenumoptions, fsrm.fsrmenumoptions, fsrmenums/FsrmEnumOptions, fsrmenums/FsrmEnumOptions_Asynchronous, fsrmenums/FsrmEnumOptions_CheckRecycleBin, fsrmenums/FsrmEnumOptions_IncludeClusterNodes, fsrmenums/FsrmEnumOptions_IncludeDeprecatedObjects, fsrmenums/FsrmEnumOptions_None
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
targetos: Windows
req.typenames: FsrmEnumOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmEnumOptions
 - fsrmenums/_FsrmEnumOptions
 - FsrmEnumOptions
 - fsrmenums/FsrmEnumOptions
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
 - FsrmEnumOptions
---

# FsrmEnumOptions enumeration


## -description

Defines the options for enumerating collections of objects.

## -enum-fields

### -field FsrmEnumOptions_None:0

Use no options and enumerate objects synchronously.

### -field FsrmEnumOptions_Asynchronous:0x1

Reserved. Do not use.

### -field FsrmEnumOptions_CheckRecycleBin:0x2

Include items and paths that are in the system recycle bin when enumerating.

### -field FsrmEnumOptions_IncludeClusterNodes:0x4

Include objects on all nodes in a <a href="/previous-versions/windows/desktop/mscs/windows-clustering">Windows cluster</a> 
      when enumerating report jobs 
      (<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>).

### -field FsrmEnumOptions_IncludeDeprecatedObjects:0x8

Include deprecated objects when enumerating.

<b>Windows Server 2008 R2 and Windows Server 2008:  </b>This enumeration value is not supported before Windows Server 2012.

## -remarks

The <b>FsrmEnumOptions_Asynchronous</b> option is not supported.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enummoduledefinitions">IFsrmClassificationManager::EnumModuleDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumpropertydefinitions">IFsrmClassificationManager::EnumPropertyDefinitions</a>



<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nf-fsrmpipeline-ifsrmclassificationmanager-enumrules">IFsrmClassificationManager::EnumRules</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-enumfilegroups">IFsrmFileGroupManager::EnumFileGroups</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjobmanager-enumfilemanagementjobs">IFsrmFileManagementJobManager::EnumFileManagementJobs</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreenexceptions">IFsrmFileScreenManager::EnumFileScreenExceptions</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreens">IFsrmFileScreenManager::EnumFileScreens</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-enumtemplates">IFsrmFileScreenTemplateManager::EnumTemplates</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">IFsrmQuotaManager::EnumAutoApplyQuotas</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumeffectivequotas">IFsrmQuotaManager::EnumEffectiveQuotas</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanagerex-isaffectedbyquota">IFsrmQuotaManagerEx::IsAffectedByQuota</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-enumtemplates">IFsrmQuotaTemplateManager::EnumTemplates</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">IFsrmReportManager::EnumReportJobs</a>
