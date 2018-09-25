---
UID: NF:fhsvcctl.FhServiceUnblockBackup
title: FhServiceUnblockBackup function
author: windows-sdk-content
description: This function unblocks backups blocked via FhServiceBlockBackup.
old-location: winprog\fhserviceunblockbackup.htm
tech.root: devnotes
ms.assetid: 4CCCEEA5-40BC-4862-ADF5-C8757E02916A
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: FhServiceUnblockBackup, FhServiceUnblockBackup function [Windows API], fhsvcctl/FhServiceUnblockBackup, winprog.fhserviceunblockbackup
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: FhSvcCtl.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - FhSvcCtl.lib
 - FhSvcCtl.dll
api_name:
 - FhServiceUnblockBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FhServiceUnblockBackup function


## -description


This function unblocks backups blocked via <a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a>.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function removes the effects of a prior <a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a> call issued via a given communication channel with the File History Service.




## -see-also




<a href="https://msdn.microsoft.com/32B5E241-5A5F-4440-9B47-07D5849FA393">FhServiceBlockBackup</a>



<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>
 

 

