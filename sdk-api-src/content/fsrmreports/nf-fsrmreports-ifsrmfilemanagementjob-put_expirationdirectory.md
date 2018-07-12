---
UID: NF:fsrmreports.IFsrmFileManagementJob.put_ExpirationDirectory
title: IFsrmFileManagementJob::put_ExpirationDirectory
author: windows-sdk-content
description: The root directory that will contain the expired files.
old-location: fsrm\ifsrmfilemanagementjob_expirationdirectory.htm
old-project: fsrm
ms.assetid: 7c8a2584-23ff-4839-b426-8f5411955746
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ExpirationDirectory property [File Server Resource Manager], ExpirationDirectory property [File Server Resource Manager],IFsrmFileManagementJob interface, IFsrmFileManagementJob interface [File Server Resource Manager],ExpirationDirectory property, IFsrmFileManagementJob.ExpirationDirectory, IFsrmFileManagementJob.put_ExpirationDirectory, IFsrmFileManagementJob::ExpirationDirectory, IFsrmFileManagementJob::get_ExpirationDirectory, IFsrmFileManagementJob::put_ExpirationDirectory, fs.ifsrmfilemanagementjob_expirationdirectory, fsrm.ifsrmfilemanagementjob_expirationdirectory, fsrmreports/IFsrmFileManagementJob::ExpirationDirectory, fsrmreports/IFsrmFileManagementJob::get_ExpirationDirectory, fsrmreports/IFsrmFileManagementJob::put_ExpirationDirectory, put_ExpirationDirectory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IFsrmFileManagementJob.ExpirationDirectory
 - IFsrmFileManagementJob.get_ExpirationDirectory
 - IFsrmFileManagementJob.put_ExpirationDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJob::put_ExpirationDirectory


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

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
    <a href="https://msdn.microsoft.com/1f48ac40-eace-49f2-b77d-2456a1a5fa34">NamespaceRoots</a> path.

Specify only if <a href="https://msdn.microsoft.com/98816ea0-7651-42ef-8893-13c568ed859a">OperationType</a> 
    is <b>FsrmFileManagementType_Expiration</b>.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

