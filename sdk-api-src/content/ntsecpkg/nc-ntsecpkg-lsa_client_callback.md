---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# LSA_CLIENT_CALLBACK callback function


## -description


The <b>ClientCallback</b> function allows a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA)-mode <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to call back to its user-mode package and invoke a function in its DLL there.


## -parameters




### -param Callback [in]

A pointer to the name of the function to invoke. For more information, see <a href="https://msdn.microsoft.com/52b4aa79-77ac-4065-a201-cc21a8d2277c">ClientCallback_Function</a>.


### -param Argument1 [in]

A pointer to the first argument to pass to the callback function.


### -param Argument2 [in]

A pointer to the second argument to pass to the callback function.


### -param Input [in]

A pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that contains information to pass to the callback function.


### -param Output [out]

A pointer to a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives information passed from the callback function.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



A pointer to the <b>ClientCallback</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.

The user-mode security package must use the 
<a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a> function to register the function to be called.




## -see-also




<a href="https://msdn.microsoft.com/52b4aa79-77ac-4065-a201-cc21a8d2277c">ClientCallback_Function</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

