---
UID: NF:shobjidl_core.IActionProgress.QueryCancel
title: IActionProgress::QueryCancel
author: windows-sdk-content
description: Provides information about whether the action is being canceled.
old-location: shell\IActionProgress_QueryCancel.htm
old-project: shell
ms.assetid: a5db4344-c1b4-4e76-9291-46dafc82e88d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IActionProgress interface [Windows Shell],QueryCancel method, IActionProgress.QueryCancel, IActionProgress::QueryCancel, QueryCancel, QueryCancel method [Windows Shell], QueryCancel method [Windows Shell],IActionProgress interface, shell.IActionProgress_QueryCancel, shell_IActionProgress_QueryCancel, shobjidl_core/IActionProgress::QueryCancel
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
-	IActionProgress.QueryCancel
product: Windows
targetos: Windows
req.lib: 
req.dll: Shobjidl.idl
req.irql: 
req.product: Outlook Express 6.0
---

# IActionProgress::QueryCancel


## -description


Provides information about whether the action is being canceled.


## -parameters




### -param pfCancelled [out]

Type: <b>BOOL*</b>

A reference to a <b>BOOL</b> value that specifies whether the action is being canceled.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks



Call this method when a process must know whether an action has been canceled. Implementing this method requires the implementing class to query either an internal or external flag to provide this information, and store the result in the value of <i>pfCancelled</i>.




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/28a2ee51-0a7a-4802-be55-f111be3a4d2d">IActionProgress::ResetCancel</a>
 

 

