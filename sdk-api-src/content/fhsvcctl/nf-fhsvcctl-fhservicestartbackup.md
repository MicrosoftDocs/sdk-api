---
UID: NF:fhsvcctl.FhServiceStartBackup
title: FhServiceStartBackup function (fhsvcctl.h)
author: windows-sdk-content
description: This function starts an immediate backup for the current user.
old-location: winprog\fhservicestartbackup.htm
tech.root: DevNotes
ms.assetid: 30800744-8605-4F8B-9B7A-50F57CC73483
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FhServiceStartBackup, FhServiceStartBackup function [Windows API], fhsvcctl/FhServiceStartBackup, winprog.fhservicestartbackup
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
 - FhServiceStartBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FhServiceStartBackup function


## -description


This function starts an immediate backup for the current user.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


### -param LowPriorityIo [in]

If <b>TRUE</b>, the File History Service is instructed to use low priority I/O for the immediate backup scheduled by this function. Low-priority I/O reduces impact on foreground user activities. It is recommended to set this parameter to <b>TRUE.</b>

If <b>FALSE</b>, the File History Service is instructed to use normal priority I/O for the immediate backup scheduled by this function. This results in faster backups but negatively affects the responsiveness and performance of user applications.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function does not wait until the immediate backup completes. If an error or warning condition is encountered during backup, it is communicated to the user via an Action Center notification and programmatically retrievable via the <a href="https://msdn.microsoft.com/662B1F54-D50D-4434-BD81-DF600D28B573">IFhConfigMgr::QueryProtectionStatus</a> method.

A backup cycle initiated by calling this function can be stopped using the <a href="https://msdn.microsoft.com/17FCD464-2543-454A-B60E-E37EDF61C595">FhServiceStopBackup</a> function.




## -see-also




<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>



<a href="https://msdn.microsoft.com/17FCD464-2543-454A-B60E-E37EDF61C595">FhServiceStopBackup</a>



<a href="https://msdn.microsoft.com/662B1F54-D50D-4434-BD81-DF600D28B573">IFhConfigMgr::QueryProtectionStatus</a>
 

 

