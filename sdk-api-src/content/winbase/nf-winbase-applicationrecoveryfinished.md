---
UID: NF:winbase.ApplicationRecoveryFinished
title: ApplicationRecoveryFinished function (winbase.h)
author: windows-sdk-content
description: Indicates that the calling application has completed its data recovery.
old-location: recovery\applicationrecoveryfinished.htm
tech.root: Recovery
ms.assetid: 2c9309c5-c36d-4b68-a642-ed087024dba1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplicationRecoveryFinished, ApplicationRecoveryFinished function [Recovery], recovery.applicationrecoveryfinished, winbase/ApplicationRecoveryFinished
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - ApplicationRecoveryFinished
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ApplicationRecoveryFinished function


## -description


Indicates that  the calling application has completed its data recovery.


## -parameters




### -param bSuccess [in]

Specify <b>TRUE</b> to indicate that the data was successfully recovered; otherwise, <b>FALSE</b>.


## -returns



This function does not return a value.




## -remarks



This should be the last call that you make in your callback because your application terminates as soon as this function is called.




## -see-also




<a href="https://msdn.microsoft.com/9c765f72-10ad-4d16-a9e5-d73ea5c4f59b">ApplicationRecoveryInProgress</a>



<a href="https://msdn.microsoft.com/4ff73c2c-a941-4626-ae40-cafbe6e50644">RegisterApplicationRecoveryCallback</a>
 

 

