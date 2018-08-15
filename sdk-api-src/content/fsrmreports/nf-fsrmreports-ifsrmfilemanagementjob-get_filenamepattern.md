---
UID: NF:fsrmreports.IFsrmFileManagementJob.get_FileNamePattern
title: IFsrmFileManagementJob::get_FileNamePattern
author: windows-sdk-content
description: A condition property:\_wildcard filter for names.
old-location: fsrm\ifsrmfilemanagementjob_filenamepattern.htm
old-project: fsrm
ms.assetid: 6a51dbc2-8e60-4575-9e97-c798e73c02a4
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FileNamePattern property [File Server Resource Manager], FileNamePattern property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],FileNamePattern property, IFsrmFileManagementJob.FileNamePattern, IFsrmFileManagementJob.get_FileNamePattern, IFsrmFileManagementJob::FileNamePattern, IFsrmFileManagementJob::get_FileNamePattern, IFsrmFileManagementJob::put_FileNamePattern, fs.ifsrmfilemanagementjob_filenamepattern, fsrm.ifsrmfilemanagementjob_filenamepattern, fsrmreports/IFsrmFileManagementJob::FileNamePattern, fsrmreports/IFsrmFileManagementJob::get_FileNamePattern, fsrmreports/IFsrmFileManagementJob::put_FileNamePattern, get_FileNamePattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmreports.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::get_FileNamePattern


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

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




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

