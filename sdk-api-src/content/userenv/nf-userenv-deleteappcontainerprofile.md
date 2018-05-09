---
UID: NF:userenv.DeleteAppContainerProfile
title: DeleteAppContainerProfile function
author: windows-driver-content
description: Deletes the specified per-user, per-app profile.
old-location: shell\deleteappcontainerprofile.htm
old-project: shell
ms.assetid: ED79D661-D087-4E44-8C32-14705ACA9D40
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DeleteAppContainerProfile, DeleteAppContainerProfile function [Windows Shell], shell.deleteappcontainerprofile, userenv/DeleteAppContainerProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
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
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	DeleteAppContainerProfile
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# DeleteAppContainerProfile function


## -description


Deletes the specified per-user, per-app profile.<div class="alert"><b>Note</b>  Deleting a non-existent profile returns success.</div>
<div> </div>



## -parameters




### -param pszAppContainerName [in]

The name given to the profile in the call to the <a href="https://msdn.microsoft.com/73F5F30F-4083-4D33-B181-31B782AD40D6">CreateAppContainerProfile</a> function. This string is at most 64 characters in length, and  fits into the pattern described by the regular expression "[-_. A-Za-z0-9]+". 


## -returns



If this function succeeds, it returns a standard HRESULT code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
If the method is called from within an app container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The profile was deleted successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
If the container name   is <b>NULL</b>, or if it exceeds its specified limit for length.

</td>
</tr>
</table>
 




## -remarks



To ensure the best results, close all file handles in the profile storage locations before calling the <b>DeleteAppContainerProfile</b> function. Otherwise, this function may not be able to completely remove the storage locations for the profile.

This function deletes the profile for the current user. To delete the profile for another user, you must impersonate that user.

If the function fails, the status of the profile is undetermined, and you should call <b>DeleteAppContainerProfile</b> again to complete the operation.




## -see-also




<a href="https://msdn.microsoft.com/73F5F30F-4083-4D33-B181-31B782AD40D6">CreateAppContainerProfile</a>
 

 

