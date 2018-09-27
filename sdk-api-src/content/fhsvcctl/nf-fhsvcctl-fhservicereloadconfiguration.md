---
UID: NF:fhsvcctl.FhServiceReloadConfiguration
title: FhServiceReloadConfiguration function
author: windows-sdk-content
description: This function causes the File History Service to reload the current user’s File History configuration files.
old-location: winprog\fhservicereloadconfiguration.htm
tech.root: devnotes
ms.assetid: DEFD729F-ED84-4C6A-8014-E986C2EB2767
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: FhServiceReloadConfiguration, FhServiceReloadConfiguration function [Windows API], fhsvcctl/FhServiceReloadConfiguration, winprog.fhservicereloadconfiguration
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
 - FhServiceReloadConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FhServiceReloadConfiguration function


## -description


This function causes the File History Service to reload the current user’s File History configuration files.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This function causes the File History Service to schedule periodic backups for the current user if they have not been scheduled yet and File History is enabled for that user.

It is recommended to call this function every time a policy is changed in File History configuration via the <a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a> method. It should also be called after File History has been enabled or disabled for a user.




## -see-also




<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>



<a href="https://msdn.microsoft.com/17FCD464-2543-454A-B60E-E37EDF61C595">FhServiceStopBackup</a>
 

 

