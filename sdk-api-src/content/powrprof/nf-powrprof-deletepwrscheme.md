---
UID: NF:powrprof.DeletePwrScheme
title: DeletePwrScheme function (powrprof.h)
author: windows-sdk-content
description: Deletes the specified power scheme.
old-location: base\deletepwrscheme.htm
tech.root: power
ms.assetid: c9513835-00c4-4260-a8b6-d947539c9dd1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeletePwrScheme, DeletePwrScheme function, _win32_deletepwrscheme, base.deletepwrscheme, powrprof/DeletePwrScheme
ms.topic: function
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - DeletePwrScheme
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeletePwrScheme function


## -description


<p class="CCE_Message">[<b>DeletePwrScheme</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="https://msdn.microsoft.com/5f9969a1-e598-4ca8-a5b8-f8bb3410223d">PowerDeleteScheme</a> instead.]

Deletes the specified power scheme.


## -parameters




### -param uiID [in]

The index of the power scheme to be deleted.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Applications can call 
<b>DeletePwrScheme</b> to permanently delete a power scheme. An attempt to delete the currently active power scheme fails with the last error set to ERROR_ACCESS_DENIED.

For more information on using PowrProf.h, see <a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>



<a href="https://msdn.microsoft.com/36052517-a85c-4512-8772-8aec31551c77">Power Schemes</a>



<a href="https://msdn.microsoft.com/b9233601-6848-41c4-bb58-27decad60ba5">WritePwrScheme</a>
 

 

