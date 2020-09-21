---
UID: NF:setupapi.SetupSetNonInteractiveMode
title: SetupSetNonInteractiveMode function (setupapi.h)
description: The SetupSetNonInteractiveMode function sets a non-interactive SetupAPI flag that determines whether SetupAPI can interact with a user in the caller's context.
helpviewer_keywords: ["SetupSetNonInteractiveMode","SetupSetNonInteractiveMode function [Device and Driver Installation]","devinst.setupsetnoninteractivemode","setup-ref_6afe961a-ba91-4ab8-b296-39308b6413c7.xml","setupapi/SetupSetNonInteractiveMode"]
old-location: devinst\setupsetnoninteractivemode.htm
tech.root: devinst
ms.assetid: 5858547d-cd0e-4067-a94b-fff58b4f1334
ms.date: 12/05/2018
ms.keywords: SetupSetNonInteractiveMode, SetupSetNonInteractiveMode function [Device and Driver Installation], devinst.setupsetnoninteractivemode, setup-ref_6afe961a-ba91-4ab8-b296-39308b6413c7.xml, setupapi/SetupSetNonInteractiveMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupSetNonInteractiveMode
 - setupapi/SetupSetNonInteractiveMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupSetNonInteractiveMode
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

Installation applications and <a href="/windows-hardware/drivers/install/writing-a-co-installer">co-installers</a> can use this function to control whether SetupAPI can display interactive user interface elements, such as dialog boxes, in the caller's context. 

An installation application or an installer can call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetnoninteractivemode">SetupGetNonInteractiveMode</a> to retrieve the current value of the non-interactive flag.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetnoninteractivemode">SetupGetNonInteractiveMode</a>