---
UID: NF:fhsvcctl.FhServiceStopBackup
title: FhServiceStopBackup function
author: windows-sdk-content
description: This function stops an ongoing backup cycle for the current user.
old-location: winprog\fhservicestopbackup.htm
tech.root: devnotes
ms.assetid: 17FCD464-2543-454A-B60E-E37EDF61C595
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FhServiceStopBackup, FhServiceStopBackup function [Windows API], fhsvcctl/FhServiceStopBackup, winprog.fhservicestopbackup
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
 - FhServiceStopBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FhServiceStopBackup function


## -description


This function stops an ongoing backup cycle for the current user.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


### -param StopTracking [in]

If <b>TRUE</b>, this function both stops the ongoing backup cycle (if any) and prevents periodic backup cycles for the current user in the future.

If <b>FALSE</b>, this function only stops the ongoing backup cycle.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -see-also




<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>
 

 

