---
UID: NF:fhsvcctl.FhServiceOpenPipe
title: FhServiceOpenPipe function
author: windows-sdk-content
description: Opens a communication channel to the File History Service.
old-location: winprog\fhserviceopenpipe.htm
tech.root: devnotes
ms.assetid: D0927124-0568-4897-9169-445C252E8ED4
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: FhServiceOpenPipe, FhServiceOpenPipe function [Windows API], fhsvcctl/FhServiceOpenPipe, winprog.fhserviceopenpipe
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
 - FhServiceOpenPipe
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FhServiceOpenPipe function


## -description


Opens a communication channel to the File History Service.


## -parameters




### -param StartServiceIfStopped [in]

If the File History Service is not started yet and this parameter is <b>TRUE</b>, this function starts the File History Service before opening a communication channel to it.

If the File History Service is not started yet and this parameter is <b>FALSE</b>, this function fails and returns an unsuccessful <b>HRESULT</b> value.


### -param Pipe [out]

On successful return, this parameter contains a non-NULL handle representing a newly opened communication channel to the File History Service.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -see-also




<a href="https://msdn.microsoft.com/20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7">FhServiceClosePipe</a>
 

 

