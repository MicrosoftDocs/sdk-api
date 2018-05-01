---
UID: NF:dskquota.DeleteUser
title: DeleteUser function
author: windows-driver-content
description: Deletes a user from the volume.
old-location: shell\DiskQuotaControl_DeleteUser.htm
old-project: shell
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DeleteUser, DeleteUser method [Windows Shell], DeleteUser method [Windows Shell], DiskQuotaControl object, DiskQuotaControl object [Windows Shell], DeleteUser method, _win32_DiskQuotaControl_DeleteUser, shell.DiskQuotaControl_DeleteUser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	DiskQuotaControl.DeleteUser
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DeleteUser function


## -description


Deletes a user from the volume.


## -parameters




### -param pUser

TBD




#### - oUser

Type: <b>Object</b>

An object expression that evaluates to the user's <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object.


## -returns



This method does not return a value.




## -remarks



This method fails if the user owns any storage on the volume. Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.




## -see-also




<a href="https://msdn.microsoft.com/de20d016-83da-42ac-962f-86faf9b25419">AddUser</a>



<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl</a>
 

 

