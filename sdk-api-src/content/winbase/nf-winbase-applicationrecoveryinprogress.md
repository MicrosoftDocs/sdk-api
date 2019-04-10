---
UID: NF:winbase.ApplicationRecoveryInProgress
title: ApplicationRecoveryInProgress function (winbase.h)
author: windows-sdk-content
description: Indicates that the calling application is continuing to recover data.
old-location: recovery\applicationrecoveryinprogress.htm
tech.root: Recovery
ms.assetid: 9c765f72-10ad-4d16-a9e5-d73ea5c4f59b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplicationRecoveryInProgress, ApplicationRecoveryInProgress function [Recovery], recovery.applicationrecoveryinprogress, winbase/ApplicationRecoveryInProgress
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
 - ApplicationRecoveryInProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ApplicationRecoveryInProgress function


## -description


Indicates that  the calling application is continuing to recover data.


## -parameters




### -param pbCancelled [out]

Indicates whether the user has canceled the recovery process. Set by WER if the user clicks the Cancel button.


## -returns



This function returns <b>S_OK</b> on success or one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
You can call this function only after Windows Error Reporting has called your recovery callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbCancelled</i> cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The application must call this function within the interval specified when calling the <a href="https://msdn.microsoft.com/4ff73c2c-a941-4626-ae40-cafbe6e50644">RegisterApplicationRecoveryCallback</a> function. If the application fails to call this function within the specified interval, WER terminates the application. The recovery process can continue as long as this function is being called.

If the user cancels the recovery process, the application should terminate. 

To indicate that the recovery process has been completed, call the <a href="https://msdn.microsoft.com/2c9309c5-c36d-4b68-a642-ed087024dba1">ApplicationRecoveryFinished</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2c9309c5-c36d-4b68-a642-ed087024dba1">ApplicationRecoveryFinished</a>



<a href="https://msdn.microsoft.com/4ff73c2c-a941-4626-ae40-cafbe6e50644">RegisterApplicationRecoveryCallback</a>
 

 

