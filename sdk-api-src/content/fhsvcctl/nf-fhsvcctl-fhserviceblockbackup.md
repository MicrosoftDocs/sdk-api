---
UID: NF:fhsvcctl.FhServiceBlockBackup
title: FhServiceBlockBackup function
author: windows-sdk-content
description: This function temporarily blocks backups for the current user.
old-location: winprog\fhserviceblockbackup.htm
old-project: devnotes
ms.assetid: 32B5E241-5A5F-4440-9B47-07D5849FA393
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FhServiceBlockBackup, FhServiceBlockBackup function [Windows API], fhsvcctl/FhServiceBlockBackup, winprog.fhserviceblockbackup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fhsvcctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - FhSvcCtl.lib
 - FhSvcCtl.dll
api_name:
 - FhServiceBlockBackup
product: Windows
targetos: Windows
req.lib: FhSvcCtl.lib
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FhServiceBlockBackup function


## -description


This function temporarily blocks backups for the current user.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function instructs the File History Service to not perform backups for the current user until the <a href="https://msdn.microsoft.com/4CCCEEA5-40BC-4862-ADF5-C8757E02916A">FhServiceUnblockBackup</a> function is called or the communication channel with the File History Service is closed by calling <a href="https://msdn.microsoft.com/20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7">FhServiceClosePipe</a>.

Call this function prior to performing File History configuration reassociation to ensure that File History configuration and data files are not currently in use. (Otherwise, the <a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a> method may fail.)




## -see-also




<a href="https://msdn.microsoft.com/20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7">FhServiceClosePipe</a>



<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>



<a href="https://msdn.microsoft.com/4CCCEEA5-40BC-4862-ADF5-C8757E02916A">FhServiceUnblockBackup</a>



<a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a>
 

 

