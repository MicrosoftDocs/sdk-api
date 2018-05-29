---
UID: NF:fsrmreports.IFsrmFileManagementJobManager.EnumFileManagementJobs
title: IFsrmFileManagementJobManager::EnumFileManagementJobs
author: windows-sdk-content
description: Enumerates the list of existing file management jobs.
old-location: fsrm\ifsrmfilemanagementjobmanager_enumfilemanagementjobs.htm
old-project: Fsrm
ms.assetid: 4af6f794-d9d4-4e03-9cd5-a4d8769888ca
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: EnumFileManagementJobs, EnumFileManagementJobs method [File Server Resource Manager], EnumFileManagementJobs method [File Server Resource Manager],FsrmFileManagementJobManager class, EnumFileManagementJobs method [File Server Resource Manager],IFsrmFileManagementJobManager interface, FsrmFileManagementJobManager class [File Server Resource Manager],EnumFileManagementJobs method, IFsrmFileManagementJobManager interface [File Server Resource Manager],EnumFileManagementJobs method, IFsrmFileManagementJobManager.EnumFileManagementJobs, IFsrmFileManagementJobManager::EnumFileManagementJobs, fs.ifsrmfilemanagementjobmanager_enumfilemanagementjobs, fsrm.ifsrmfilemanagementjobmanager_enumfilemanagementjobs, fsrmreports/IFsrmFileManagementJobManager::EnumFileManagementJobs
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileManagementJobManager.EnumFileManagementJobs
-	FsrmFileManagementJobManager.EnumFileManagementJobs
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileManagementJobManager::EnumFileManagementJobs


## -description


Enumerates the list of existing file management jobs.


## -parameters




### -param options [in]

One or more options to use when enumerating the management jobs. For possible values, see the <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  This parameter must be set to either <b>FsrmEnumOptions_IncludeClusterNodes</b> or <b>FsrmEnumOptions_None</b> for this method.</div>
<div> </div>

### -param fileManagementJobs [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a collection of file management jobs.  The variant type of each item in the collection is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant to get an <a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a> interface to the job.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/f59844ba-2aff-4885-b80b-82f3e1a638d3">FsrmFileManagementJobManager</a>



<a href="https://msdn.microsoft.com/2df0e8d0-1da7-422e-8d02-ad5d030fdd8d">IFsrmFileManagementJobManager</a>



<a href="https://msdn.microsoft.com/106c5237-94bc-4556-aa65-247697133810">IFsrmFileManagementJobManager::GetFileManagementJob</a>
 

 

