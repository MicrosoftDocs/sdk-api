---
UID: NF:shobjidl_core.IExecuteCommandApplicationHostEnvironment.GetValue
title: IExecuteCommandApplicationHostEnvironment::GetValue
author: windows-sdk-content
description: Determines whether the current application host environment is in the desktop or immersive mode.
old-location: shell\IExecuteCommandApplicationHostEnvironment_GetValue.htm
tech.root: shell
ms.assetid: ba26f985-04f1-4a05-9363-a7be0585bcfc
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AHE_DESKTOP, AHE_IMMERSIVE, GetValue, GetValue method [Windows Shell], GetValue method [Windows Shell],IExecuteCommandApplicationHostEnvironment interface, IExecuteCommandApplicationHostEnvironment interface [Windows Shell],GetValue method, IExecuteCommandApplicationHostEnvironment.GetValue, IExecuteCommandApplicationHostEnvironment::GetValue, shell.IExecuteCommandApplicationHostEnvironment_GetValue, shobjidl_core/IExecuteCommandApplicationHostEnvironment::GetValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExecuteCommandApplicationHostEnvironment.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c890d306-66df-4c29-88db-d54362ac018a">IExecuteCommandApplicationHostEnvironment</a>
 

 

