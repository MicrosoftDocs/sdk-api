---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_ExpirationDirectory
title: IFsrmFileManagementJob::put_ExpirationDirectory (fsrmreports.h)
description: The root directory that will contain the expired files.
helpviewer_keywords: ["ExpirationDirectory property [File Server Resource Manager]","ExpirationDirectory property [File Server Resource Manager]","IFsrmFileManagementJob interface","IFsrmFileManagementJob interface [File Server Resource Manager]","ExpirationDirectory property","IFsrmFileManagementJob.ExpirationDirectory","IFsrmFileManagementJob.put_ExpirationDirectory","IFsrmFileManagementJob::ExpirationDirectory","IFsrmFileManagementJob::get_ExpirationDirectory","IFsrmFileManagementJob::put_ExpirationDirectory","fs.ifsrmfilemanagementjob_expirationdirectory","fsrm.ifsrmfilemanagementjob_expirationdirectory","fsrmreports/IFsrmFileManagementJob::ExpirationDirectory","fsrmreports/IFsrmFileManagementJob::get_ExpirationDirectory","fsrmreports/IFsrmFileManagementJob::put_ExpirationDirectory","put_ExpirationDirectory"]
old-location: fsrm\ifsrmfilemanagementjob_expirationdirectory.htm
tech.root: fsrm
ms.assetid: 7c8a2584-23ff-4839-b426-8f5411955746
ms.date: 12/05/2018
ms.keywords: ExpirationDirectory property [File Server Resource Manager], ExpirationDirectory property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],ExpirationDirectory property, IFsrmFileManagementJob.ExpirationDirectory, IFsrmFileManagementJob.put_ExpirationDirectory, IFsrmFileManagementJob::ExpirationDirectory, IFsrmFileManagementJob::get_ExpirationDirectory, IFsrmFileManagementJob::put_ExpirationDirectory, fs.ifsrmfilemanagementjob_expirationdirectory, fsrm.ifsrmfilemanagementjob_expirationdirectory, fsrmreports/IFsrmFileManagementJob::ExpirationDirectory, fsrmreports/IFsrmFileManagementJob::get_ExpirationDirectory, fsrmreports/IFsrmFileManagementJob::put_ExpirationDirectory, put_ExpirationDirectory
f1_keywords:
- fsrmreports/IFsrmFileManagementJob.ExpirationDirectory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmFileManagementJob.ExpirationDirectory
- IFsrmFileManagementJob.get_ExpirationDirectory
- IFsrmFileManagementJob.put_ExpirationDirectory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJob::put_ExpirationDirectory


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a> class.]

The root directory that will contain the expired files.

This property is read/write.


## -parameters


## -remarks



FSRM moves the files that meet all of the file management job's conditions to this directory when the job is 
    run, therefore the running process must have write permission. The directory must also be located on an NTFS 
    volume.

FSRM maintains the file's current directory structure in the expired directory so you can determine its 
     previous location. For example, if FSRM expired the file, 
     "C:\TestExpired\Test1.txt", the expired root directory would contain:

"<i>FsrmServer(FQDN)</i>\<i>JobName</i>_<i>TimeStamp</i>\C$\TestExpired\Test1.txt"

The expired file's ACLs are maintained with the file.

If the expiration directory does not exist, FSRM creates the directory (with administrator access rights 
     only).

Do not specify an expiration directory that is in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_namespaceroots">NamespaceRoots</a> path.

Specify only if <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmfilemanagementjob-get_operationtype">OperationType</a> 
    is <b>FsrmFileManagementType_Expiration</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjob">IFsrmFileManagementJob</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilemanagementjob">MSFT_FSRMFileManagementJob</a>
 

 

