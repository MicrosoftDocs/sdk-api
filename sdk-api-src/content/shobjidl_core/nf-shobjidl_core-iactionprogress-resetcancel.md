---
UID: NF:shobjidl_core.IActionProgress.ResetCancel
title: IActionProgress::ResetCancel
author: windows-sdk-content
description: Resets progress dialog after a cancellation has been completed.
old-location: shell\IActionProgress_ResetCancel.htm
old-project: shell
ms.assetid: 28a2ee51-0a7a-4802-be55-f111be3a4d2d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IActionProgress interface [Windows Shell],ResetCancel method, IActionProgress.ResetCancel, IActionProgress::ResetCancel, ResetCancel, ResetCancel method [Windows Shell], ResetCancel method [Windows Shell],IActionProgress interface, shell.IActionProgress_ResetCancel, shell_IActionProgress_ResetCancel, shobjidl_core/IActionProgress::ResetCancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
-	Shobjidl.idl
api_name:
-	IActionProgress.ResetCancel
product: Windows
targetos: Windows
req.lib: 
req.dll: Shobjidl.idl
req.irql: 
req.product: Outlook Express 6.0
---

# IActionProgress::ResetCancel


## -description


Resets progress dialog after a cancellation has been completed.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks



This method is called when a cancellation has been completed. User input should typically be limited for cancellations of actions that involve large calculations or file operations. This method may be used by calling applications to notify a progress UI that the cancellation has been completed and the UI should return control to the user.




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/a5db4344-c1b4-4e76-9291-46dafc82e88d">IActionProgress::QueryCancel</a>
 

 

