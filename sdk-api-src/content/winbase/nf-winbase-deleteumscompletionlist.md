---
UID: NF:winbase.DeleteUmsCompletionList
title: DeleteUmsCompletionList function
author: windows-sdk-content
description: Deletes the specified user-mode scheduling (UMS) completion list. The list must be empty.
old-location: base\deleteumscompletionlist.htm
old-project: ProcThread
ms.assetid: 98124359-ddd1-468c-9f99-74dd3f631fa1
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DeleteUmsCompletionList, DeleteUmsCompletionList function, base.deleteumscompletionlist, winbase/DeleteUmsCompletionList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-ums-l1-1-0.dll
api_name:
-	DeleteUmsCompletionList
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteUmsCompletionList function


## -description


Deletes the specified user-mode scheduling (UMS) completion list. The list must be empty.


## -parameters




### -param UmsCompletionList [in]

A pointer to the UMS completion list to be deleted. The <a href="https://msdn.microsoft.com/6e77b793-a82e-4e23-8c8b-7aff79d69346">CreateUmsCompletionList</a> function provides this pointer.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the completion list is shared, the caller is responsible for ensuring that no active UMS thread holds a reference to the list before deleting it.



