---
UID: NF:winbase.UnregisterApplicationRestart
title: UnregisterApplicationRestart function (winbase.h)
author: windows-sdk-content
description: Removes the active instance of an application from the restart list.
old-location: recovery\unregisterapplicationrestart.htm
tech.root: Recovery
ms.assetid: 7491812d-6469-4ac3-8d51-68b9c4b13b29
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnregisterApplicationRestart, UnregisterApplicationRestart function [Recovery], recovery.unregisterapplicationrestart, winbase/UnregisterApplicationRestart
ms.topic: function
f1_keywords: ["winbase/UnregisterApplicationRestart"]
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
 - UnregisterApplicationRestart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart">RegisterApplicationRestart</a>
 

 

