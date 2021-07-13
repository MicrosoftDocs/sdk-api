---
UID: NF:setupapi.SetupGetNonInteractiveMode
title: SetupGetNonInteractiveMode function (setupapi.h)
description: The SetupGetNonInteractiveMode function returns the value of a SetupAPI non-interactive flag that indicates whether the caller's process can interact with a user through user interface components, such as dialog boxes.
helpviewer_keywords: ["SetupGetNonInteractiveMode","SetupGetNonInteractiveMode function [Device and Driver Installation]","devinst.setupgetnoninteractivemode","setup-ref_c292cd64-d95d-4e1a-a28b-183ad013bbd3.xml","setupapi/SetupGetNonInteractiveMode"]
old-location: devinst\setupgetnoninteractivemode.htm
tech.root: devinst
ms.assetid: 0978851d-18a6-47a3-8ac9-0c03c469cbef
ms.date: 12/05/2018
ms.keywords: SetupGetNonInteractiveMode, SetupGetNonInteractiveMode function [Device and Driver Installation], devinst.setupgetnoninteractivemode, setup-ref_c292cd64-d95d-4e1a-a28b-183ad013bbd3.xml, setupapi/SetupGetNonInteractiveMode
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
 - SetupGetNonInteractiveMode
 - setupapi/SetupGetNonInteractiveMode
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
 - SetupGetNonInteractiveMode
---

# SetupGetNonInteractiveMode function


## -description

The <b>SetupGetNonInteractiveMode</b> function returns the value of a SetupAPI non-interactive flag  that indicates whether the caller's process can interact with a user through user interface components, such as dialog boxes.



## -returns

<b>SetupGetNonInteractiveMode</b> returns <b>TRUE</b> if the caller's process cannot display interactive user interface elements, such as dialog boxes. Otherwise, the function returns <b>FALSE</b>, which indicates that the process can display interactive user interface elements.

## -remarks

Installation applications and <a href="/windows-hardware/drivers/install/writing-a-co-installer">co-installers</a> can use this function to determine whether the current process can display interactive user interface elements such as dialog boxes. <a href="/windows-hardware/drivers/install/setupapi">SetupAPI</a> runs a class installer or a co-installer either in an interactive or in a non-interactive process, depending on which <a href="/windows-hardware/drivers/install/handling-dif-codes">DIF code</a> SetupAPI is processing.

An installation application can call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetnoninteractivemode">SetupSetNonInteractiveMode</a> to set the SetupAPI non-interactive flag that controls whether SetupAPI can display interactive user interface elements in the caller's context.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetnoninteractivemode">SetupSetNonInteractiveMode</a>
