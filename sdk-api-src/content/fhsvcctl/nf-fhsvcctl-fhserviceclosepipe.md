---
UID: NF:fhsvcctl.FhServiceClosePipe
title: FhServiceClosePipe function
author: windows-sdk-content
description: Closes a communication channel to the File History Service opened with FhServiceOpenPipe.
old-location: winprog\fhserviceclosepipe.htm
old-project: devnotes
ms.assetid: 20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FhServiceClosePipe, FhServiceClosePipe function [Windows API], fhsvcctl/FhServiceClosePipe, winprog.fhserviceclosepipe
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
 - FhServiceClosePipe
product: Windows
targetos: Windows
req.lib: FhSvcCtl.lib
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FhServiceClosePipe function


## -description


Closes a communication channel to the File History Service opened with <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>.


## -parameters




### -param Pipe [in]

The communication channel handle returned by an earlier <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a> call.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



An application should call <b>FhServiceClosePipe</b> once for each communication channel handle it opens with <a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>. Closing a communication channel handle multiple times is not supported and may lead to unpredictable behavior.




## -see-also




<a href="https://msdn.microsoft.com/D0927124-0568-4897-9169-445C252E8ED4">FhServiceOpenPipe</a>
 

 

