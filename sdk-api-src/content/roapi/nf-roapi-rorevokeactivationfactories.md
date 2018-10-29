---
UID: NF:roapi.RoRevokeActivationFactories
title: RoRevokeActivationFactories function
author: windows-sdk-content
description: Removes an array of registered activation factories from the Windows Runtime.
old-location: winrt\rorevokeactivationfactories.htm
tech.root: WinRT
ms.assetid: 0311bd92-3b12-46bc-a21d-13bd57a2c545
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RoRevokeActivationFactories, RoRevokeActivationFactories function [Windows Runtime], WinRTRevokeActivationFactories, roapi/RoRevokeActivationFactories, roapi/WinRTRevokeActivationFactories, winrt.rorevokeactivationfactories, winrt.winrtrevokeactivationfactories
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-l1-1-0.dll
api_name:
 - RoRevokeActivationFactories
 - WinRTRevokeActivationFactories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RoRevokeActivationFactories function


## -description


Removes an array of registered activation factories from the Windows Runtime.


## -parameters




### -param cookie [in]

Type: <b><a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a></b>


## -returns



This function does not return a value.




## -remarks



Call the <b>RoRevokeActivationFactories</b> function remove the activation factories represented in the  <i>cookie</i> array from the Windows Runtime.




## -see-also




<a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a>



<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>



<a href="https://msdn.microsoft.com/8213f5de-3b1c-44c3-ad37-b2ebac8dbcd8">RoRegisterActivationFactories</a>
 

 

