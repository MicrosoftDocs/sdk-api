---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_FileNamePattern
title: IFsrmFileManagementJob::get_FileNamePattern (fsrmreports.h)
description: A condition property:\_wildcard filter for names. (Get)
helpviewer_keywords: ["FileNamePattern property [File Server Resource Manager]","FileNamePattern property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","FileNamePattern property","IFsrmFileManagementJob.FileNamePattern","IFsrmFileManagementJob.get_FileNamePattern","IFsrmFileManagementJob::FileNamePattern","IFsrmFileManagementJob::get_FileNamePattern","IFsrmFileManagementJob::put_FileNamePattern","fs.ifsrmfilemanagementjob_filenamepattern","fsrm.ifsrmfilemanagementjob_filenamepattern","fsrmreports/IFsrmFileManagementJob::FileNamePattern","fsrmreports/IFsrmFileManagementJob::get_FileNamePattern","fsrmreports/IFsrmFileManagementJob::put_FileNamePattern","get_FileNamePattern"]
old-location: fsrm\ifsrmfilemanagementjob_filenamepattern.htm
tech.root: fsrm
ms.assetid: 6a51dbc2-8e60-4575-9e97-c798e73c02a4
ms.date: 12/05/2018
ms.keywords: FileNamePattern property [File Server Resource Manager], FileNamePattern property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],FileNamePattern property, IFsrmFileManagementJob.FileNamePattern, IFsrmFileManagementJob.get_FileNamePattern, IFsrmFileManagementJob::FileNamePattern, IFsrmFileManagementJob::get_FileNamePattern, IFsrmFileManagementJob::put_FileNamePattern, fs.ifsrmfilemanagementjob_filenamepattern, fsrm.ifsrmfilemanagementjob_filenamepattern, fsrmreports/IFsrmFileManagementJob::FileNamePattern, fsrmreports/IFsrmFileManagementJob::get_FileNamePattern, fsrmreports/IFsrmFileManagementJob::put_FileNamePattern, get_FileNamePattern
req.header: fsrmreports.h
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
 - IFsrmFileManagementJob::get_FileNamePattern
 - fsrmreports/IFsrmFileManagementJob::get_FileNamePattern
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
 - IFsrmFileManagementJob.FileNamePattern
 - IFsrmFileManagementJob.get_FileNamePattern
 - IFsrmFileManagementJob.put_FileNamePattern
---

# IFsrmFileManagementJob::get_FileNamePattern


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

A condition property: wildcard filter for names.

This property is read/write.

## -parameters

## -remarks

A file name pattern is a string expression that defines a set of file names. The expression may contain the 
    following wildcard characters: "*" and "?". The "*" wildcard 
    matches zero or more characters and the "?" wildcard  matches exactly 1 character. For example, 
    the file name "example.cpp" matches the pattern "e*.cpp", but not "e?.cpp". The file name "ex.cpp" would match 
    both patterns. Note that when the file name pattern is used to compare against a specific file name, the pattern 
    match is case-insensitive.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
