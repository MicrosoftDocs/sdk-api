---
UID: NF:shellapi.NetAddr_DisplayErrorTip
title: NetAddr_DisplayErrorTip macro
author: windows-sdk-content
description: Displays an error message in the balloon tip associated with the network address control.
old-location: shell\NetAddr_DisplayErrorTip.htm
old-project: shell
ms.assetid: 1fd623da-51a0-4b37-a25b-00278b5f4732
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NetAddr_DisplayErrorTip, NetAddr_DisplayErrorTip macro [Windows Shell], _shell_NetAddr_DisplayErrorTip, shell.NetAddr_DisplayErrorTip, shellapi/NetAddr_DisplayErrorTip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SHSTOCKICONID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shellapi.h
api_name:
-	NetAddr_DisplayErrorTip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# NetAddr_DisplayErrorTip macro


## -description


Displays an error message in the balloon tip associated with the network address control.


## -parameters




### -param hwnd [in]

A handle to the network address control.


## -remarks



Call this macro to display an error message when an address typed into the control does not validate against the allowed network address types set with macro <a href="https://msdn.microsoft.com/2fa97abd-79c8-41ce-bd0e-75941bf4d005">NetAddr_SetAllowType</a>. Use the macro <a href="https://msdn.microsoft.com/2d0310a8-89ca-41b5-8afc-faec29bd23ba">NetAddr_GetAddress</a> to validate the address.




## -see-also




<a href="https://msdn.microsoft.com/21533513-86c2-418b-ab62-3c1b2db9bc2f">NetAddr_GetAllowType</a>
 

 

