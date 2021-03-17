---
UID: NF:fsrmpipeline.IFsrmRule.get_LastModified
title: IFsrmRule::get_LastModified (fsrmpipeline.h)
description: The date for the last time the rule was modified.
helpviewer_keywords: ["IFsrmRule interface [File Server Resource Manager]","LastModified property","IFsrmRule.LastModified","IFsrmRule.get_LastModified","IFsrmRule::LastModified","IFsrmRule::get_LastModified","LastModified property [File Server Resource Manager]","LastModified property [File Server Resource Manager]","IFsrmRule interface","fs.ifsrmrule_lastmodified","fsrm.ifsrmrule_lastmodified","fsrmpipeline/IFsrmRule::LastModified","fsrmpipeline/IFsrmRule::get_LastModified","get_LastModified"]
old-location: fsrm\ifsrmrule_lastmodified.htm
tech.root: fsrm
ms.assetid: 8f087d75-6432-40d3-b9bf-aec3733a7107
ms.date: 12/05/2018
ms.keywords: IFsrmRule interface [File Server Resource Manager],LastModified property, IFsrmRule.LastModified, IFsrmRule.get_LastModified, IFsrmRule::LastModified, IFsrmRule::get_LastModified, LastModified property [File Server Resource Manager], LastModified property [File Server Resource Manager],IFsrmRule interface, fs.ifsrmrule_lastmodified, fsrm.ifsrmrule_lastmodified, fsrmpipeline/IFsrmRule::LastModified, fsrmpipeline/IFsrmRule::get_LastModified, get_LastModified
req.header: fsrmpipeline.h
req.include-header: 
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmRule::get_LastModified
 - fsrmpipeline/IFsrmRule::get_LastModified
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmRule.LastModified
 - IFsrmRule.get_LastModified
---

# IFsrmRule::get_LastModified


## -description

The date for the last time the rule was modified.

This property is read-only.

## -parameters

## -remarks

The last-modified time is set each time you commit the rule.

The last-modified time is used by FSRM to determine whether the rule needs to be run. If any rule returns a time that is more recent than the time a file was last modified, FSRM will re-evaluate any applicable rules for that file.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmrule">IFsrmRule</a>