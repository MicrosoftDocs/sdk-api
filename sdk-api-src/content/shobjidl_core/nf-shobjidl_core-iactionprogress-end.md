---
UID: NF:shobjidl_core.IActionProgress.End
title: IActionProgress::End (shobjidl_core.h)
author: windows-sdk-content
description: Indicates that the action associated with this progress implementation has ended.
old-location: shell\IActionProgress_End.htm
tech.root: shell
ms.assetid: 91fa11c3-c781-4e96-9a42-4625b8b24333
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: End, End method [Windows Shell], End method [Windows Shell],IActionProgress interface, IActionProgress interface [Windows Shell],End method, IActionProgress.End, IActionProgress::End, shell.IActionProgress_End, shell_IActionProgress_End, shobjidl_core/IActionProgress::End
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
req.lib: 
req.dll: Shobjidl.idl
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.idl
api_name:
 - IActionProgress.End
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActionProgress::End


## -description


Indicates that the action associated with this progress implementation has ended.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks



This method indicates that the action has finished, and the implementing class should perform cleanup and display results to the user, if applicable.
		




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/c26dd072-6d59-4c6c-a273-682ded994612">IActionProgress::Begin</a>
 

 

