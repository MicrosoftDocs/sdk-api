---
UID: NF:shobjidl_core.IExecuteCommandApplicationHostEnvironment.GetValue
title: IExecuteCommandApplicationHostEnvironment::GetValue (shobjidl_core.h)
description: Determines whether the current application host environment is in the desktop or immersive mode.
helpviewer_keywords: ["AHE_DESKTOP","AHE_IMMERSIVE","GetValue","GetValue method [Windows Shell]","GetValue method [Windows Shell]","IExecuteCommandApplicationHostEnvironment interface","IExecuteCommandApplicationHostEnvironment interface [Windows Shell]","GetValue method","IExecuteCommandApplicationHostEnvironment.GetValue","IExecuteCommandApplicationHostEnvironment::GetValue","shell.IExecuteCommandApplicationHostEnvironment_GetValue","shobjidl_core/IExecuteCommandApplicationHostEnvironment::GetValue"]
old-location: shell\IExecuteCommandApplicationHostEnvironment_GetValue.htm
tech.root: shell
ms.assetid: ba26f985-04f1-4a05-9363-a7be0585bcfc
ms.date: 12/05/2018
ms.keywords: AHE_DESKTOP, AHE_IMMERSIVE, GetValue, GetValue method [Windows Shell], GetValue method [Windows Shell],IExecuteCommandApplicationHostEnvironment interface, IExecuteCommandApplicationHostEnvironment interface [Windows Shell],GetValue method, IExecuteCommandApplicationHostEnvironment.GetValue, IExecuteCommandApplicationHostEnvironment::GetValue, shell.IExecuteCommandApplicationHostEnvironment_GetValue, shobjidl_core/IExecuteCommandApplicationHostEnvironment::GetValue
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExecuteCommandApplicationHostEnvironment::GetValue
 - shobjidl_core/IExecuteCommandApplicationHostEnvironment::GetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExecuteCommandApplicationHostEnvironment.GetValue
---

# IExecuteCommandApplicationHostEnvironment::GetValue


## -description

Determines whether the current application host environment is in the desktop or immersive mode.

## -parameters

### -param pahe [out]

A pointer to a <b>AHE_TYPE</b> value that, when this method returns successfully, receives one of the following values to indicate the current host environment.



#### AHE_DESKTOP (0)

Desktop.



#### AHE_IMMERSIVE (1)

Immersive mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment">IExecuteCommandApplicationHostEnvironment</a>