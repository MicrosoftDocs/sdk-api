---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetKey
title: IDefaultExtractIconInit::SetKey
author: windows-driver-content
description: Sets the registry key from which to load the &#0034;DefaultIcon&#0034; value.
old-location: shell\IDefaultExtractIconInit_SetKey.htm
old-project: shell
ms.assetid: dce75b90-f569-4983-a540-82a021377287
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetKey method, IDefaultExtractIconInit.SetKey, IDefaultExtractIconInit::SetKey, SetKey, SetKey method [Windows Shell], SetKey method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetKey, shell.IDefaultExtractIconInit_SetKey, shobjidl_core/IDefaultExtractIconInit::SetKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IDefaultExtractIconInit.SetKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDefaultExtractIconInit::SetKey


## -description


Sets the registry key from which to load the "DefaultIcon" value.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

A handle to the registry key.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that any call to <b>IDefaultExtractIconInit::SetKey</b> come before any calls to the SetXxxIcon methods.



