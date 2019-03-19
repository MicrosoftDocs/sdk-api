---
UID: NF:winbase.UnregisterApplicationRecoveryCallback
title: UnregisterApplicationRecoveryCallback function (winbase.h)
author: windows-sdk-content
description: Removes the active instance of an application from the recovery list.
old-location: recovery\unregisterapplicationrecoverycallback.htm
tech.root: Recovery
ms.assetid: 473e24d6-fddb-4935-b454-8cddfb53a02a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UnregisterApplicationRecoveryCallback, UnregisterApplicationRecoveryCallback function [Recovery], recovery.unregisterapplicationrecoverycallback, winbase/UnregisterApplicationRecoveryCallback
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
 - UnregisterApplicationRecoveryCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnregisterApplicationRecoveryCallback function


## -description


Removes the active instance of an application from the recovery list.


## -parameters






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
Internal error.

</td>
</tr>
</table>
 




## -remarks



You do not need to call this function before exiting. You need to remove the registration only if you choose to not recover data.




## -see-also




<a href="https://msdn.microsoft.com/4ff73c2c-a941-4626-ae40-cafbe6e50644">RegisterApplicationRecoveryCallback</a>
 

 

