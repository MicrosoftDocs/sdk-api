---
UID: NF:fsrmpipeline.IFsrmClassifierModuleImplementation.get_LastModified
title: IFsrmClassifierModuleImplementation::get_LastModified (fsrmpipeline.h)
description: The last time the classifier's internal rules were modified as a 64-bit FILETIME value.
helpviewer_keywords: ["FsrmAlwaysModified","FsrmNeverModified","IFsrmClassifierModuleImplementation interface [File Server Resource Manager]","LastModified property","IFsrmClassifierModuleImplementation.LastModified","IFsrmClassifierModuleImplementation.get_LastModified","IFsrmClassifierModuleImplementation::LastModified","IFsrmClassifierModuleImplementation::get_LastModified","LastModified property [File Server Resource Manager]","LastModified property [File Server Resource Manager]","IFsrmClassifierModuleImplementation interface","fs.ifsrmclassifiermoduleimplementation_lastmodified","fsrm.ifsrmclassifiermoduleimplementation_lastmodified","fsrmpipeline/IFsrmClassifierModuleImplementation::LastModified","fsrmpipeline/IFsrmClassifierModuleImplementation::get_LastModified","get_LastModified"]
old-location: fsrm\ifsrmclassifiermoduleimplementation_lastmodified.htm
tech.root: fsrm
ms.assetid: edda630a-947d-4c81-b4d5-c02b3ba02f10
ms.date: 12/05/2018
ms.keywords: FsrmAlwaysModified, FsrmNeverModified, IFsrmClassifierModuleImplementation interface [File Server Resource Manager],LastModified property, IFsrmClassifierModuleImplementation.LastModified, IFsrmClassifierModuleImplementation.get_LastModified, IFsrmClassifierModuleImplementation::LastModified, IFsrmClassifierModuleImplementation::get_LastModified, LastModified property [File Server Resource Manager], LastModified property [File Server Resource Manager],IFsrmClassifierModuleImplementation interface, fs.ifsrmclassifiermoduleimplementation_lastmodified, fsrm.ifsrmclassifiermoduleimplementation_lastmodified, fsrmpipeline/IFsrmClassifierModuleImplementation::LastModified, fsrmpipeline/IFsrmClassifierModuleImplementation::get_LastModified, get_LastModified
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
 - IFsrmClassifierModuleImplementation::get_LastModified
 - fsrmpipeline/IFsrmClassifierModuleImplementation::get_LastModified
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
 - IFsrmClassifierModuleImplementation.LastModified
 - IFsrmClassifierModuleImplementation.get_LastModified
---

# IFsrmClassifierModuleImplementation::get_LastModified


## -description

The last time the classifier's internal rules were modified as a 64-bit FILETIME value.

This property is read-only.

## -parameters

## -remarks

The last modified time is used by FSRM to determine whether rules using this classifier need to be run. If any classifier returns a time that is more recent than the time a file was last modified, FSRM will re-evaluate any applicable rules for that file.

A value corresponding to <b>FsrmNeverModified</b> can be returned if the classifier has no internal policies that are ever updated. An example of such a classifier is one that bases its classification decision on the attributes (such as path or owner) or content of a file.

A value corresponding to <b>FsrmAlwaysModified</b> can be returned if the classifier has internal policies that affect rules that always need to be reevaluated on each classification run. In this case, applicable rules for each file will always be evaluated. An example of such a classifier is one that bases its classification decision on a volatile set of policies that are outside the control of FSRM. A classifier that returns <b>FsrmAlwaysModified</b> will affect the performance of file classification because in such cases FSRM will skip optimizations that normally can avoid unnecessary rule reevaluations.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmpipeline/nn-fsrmpipeline-ifsrmclassifiermoduleimplementation">IFsrmClassifierModuleImplementation</a>