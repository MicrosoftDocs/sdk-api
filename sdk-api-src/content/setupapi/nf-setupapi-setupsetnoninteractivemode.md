---
UID: NF:setupapi.SetupSetNonInteractiveMode
title: SetupSetNonInteractiveMode function
author: windows-sdk-content
description: The SetupSetNonInteractiveMode function sets a non-interactive SetupAPI flag that determines whether SetupAPI can interact with a user in the caller's context.
old-location: devinst\setupsetnoninteractivemode.htm
tech.root: devinst
ms.assetid: 5858547d-cd0e-4067-a94b-fff58b4f1334
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetupSetNonInteractiveMode, SetupSetNonInteractiveMode function [Device and Driver Installation], devinst.setupsetnoninteractivemode, setup-ref_6afe961a-ba91-4ab8-b296-39308b6413c7.xml, setupapi/SetupSetNonInteractiveMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupSetNonInteractiveMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupSetNonInteractiveMode function


## -description


The <b>SetupSetNonInteractiveMode</b> function sets a non-interactive SetupAPI flag that determines whether SetupAPI can interact with a user in the caller's context. 


## -parameters




### -param NonInteractiveFlag [in]

The Boolean value of the non-interactive flag. If <i>NonInteractive</i> is set to <b>TRUE</b>, SetupAPI runs in a non-interactive user mode and if <i>NonInteractive</i> is set to <b>FALSE</b>, SetupAPI runs in an interactive user mode.


## -returns



<b>SetupSetNonInteractiveMode</b> returns the previous setting of the non-interactive flag.




## -remarks



Installation applications and <a href="devinst.writing_a_co_installer">co-installers</a> can use this function to control whether SetupAPI can display interactive user interface elements, such as dialog boxes, in the caller's context. 

An installation application or an installer can call <a href="https://msdn.microsoft.com/0978851d-18a6-47a3-8ac9-0c03c469cbef">SetupGetNonInteractiveMode</a> to retrieve the current value of the non-interactive flag. 




## -see-also




<a href="https://msdn.microsoft.com/0978851d-18a6-47a3-8ac9-0c03c469cbef">SetupGetNonInteractiveMode</a>
 

 

