---
UID: NF:winnt.TpSetCallbackCleanupGroup
title: TpSetCallbackCleanupGroup function
author: windows-sdk-content
description: Associates the specified cleanup group with the specified callback environment.
old-location: base\tpsetcallbackcleanupgroup.htm
old-project: ProcThread
ms.assetid: B14084F5-2686-4522-8024-71A07541CFE2
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: TpSetCallbackCleanupGroup, TpSetCallbackCleanupGroup function, base.tpsetcallbackcleanupgroup, winnt/TpSetCallbackCleanupGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winnt.h
api_name:
-	TpSetCallbackCleanupGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TpSetCallbackCleanupGroup function


## -description


Associates the specified cleanup group with the specified callback environment.


## -parameters




### -param CallbackEnviron [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a> function returns this structure.


### -param CleanupGroup [in]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a> function returns this structure.


### -param CleanupGroupCancelCallback [in, optional]

The cleanup callback to be called if the cleanup group is canceled before the associated object is released. The function is called when you call <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>.


## -returns



This function does not return a value.




## -remarks



This function is implemented as an inline function.




## -see-also




<a href="https://msdn.microsoft.com/B0925491-73FE-4342-9E66-E5F6344353FB">TpDestroyCallbackEnviron</a>



<a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a>



<a href="https://msdn.microsoft.com/C4715789-0DF7-436B-881F-4360A7528246">TpSetCallbackActivationContext</a>



<a href="https://msdn.microsoft.com/425898A7-5E98-490A-912A-A409D1E2DFDE">TpSetCallbackFinalizationCallback</a>



<a href="https://msdn.microsoft.com/27E7F647-1005-4499-9787-F2CE6E8B6AFF">TpSetCallbackLongFunction</a>



<a href="https://msdn.microsoft.com/8415197A-C785-492E-9C74-2055FADDF0CD">TpSetCallbackNoActivationContext</a>



<a href="https://msdn.microsoft.com/FE2CB959-25BC-4420-A921-2A65016B25CF">TpSetCallbackPersistent</a>



<a href="https://msdn.microsoft.com/3A2DA8CA-D5F2-442A-B152-11AB28681B5B">TpSetCallbackPriority</a>



<a href="https://msdn.microsoft.com/14519064-450C-409E-AA2D-B4EF4D43C180">TpSetCallbackRaceWithDll</a>



<a href="https://msdn.microsoft.com/A1BED20A-9DB5-4B5A-B1AD-60454176AB1D">TpSetCallbackThreadpool</a>
 

 

