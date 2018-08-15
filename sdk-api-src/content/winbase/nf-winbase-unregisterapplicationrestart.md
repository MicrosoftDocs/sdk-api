---
UID: NF:winbase.UnregisterApplicationRestart
title: UnregisterApplicationRestart function
author: windows-sdk-content
description: Removes the active instance of an application from the restart list.
old-location: recovery\unregisterapplicationrestart.htm
old-project: recovery
ms.assetid: 7491812d-6469-4ac3-8d51-68b9c4b13b29
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UnregisterApplicationRestart, UnregisterApplicationRestart function [Recovery], recovery.unregisterapplicationrestart, winbase/UnregisterApplicationRestart
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - UnregisterApplicationRestart
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# UnregisterApplicationRestart function


## -description


Removes the active instance of an application from the restart list.


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



You do not need to call this function before exiting. You need to remove the registration only if you choose to not restart the application. For example, you could remove the registration if your application entered a corrupted state where a future restart would also fail. You must call this function before the application fails abnormally.




## -see-also




<a href="https://msdn.microsoft.com/f4cd25b3-2aee-460f-9f9f-b45ecded094f">RegisterApplicationRestart</a>
 

 

