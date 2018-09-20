---
UID: NF:shobjidl_core.IObjectWithBackReferences.RemoveBackReferences
title: IObjectWithBackReferences::RemoveBackReferences
author: windows-sdk-content
description: Removes all back references held by an object.
old-location: shell\IObjectWithBackReferences_RemoveBackReferences.htm
tech.root: shell
ms.assetid: 642fe793-974f-48e5-90a2-de6ba7a5b033
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IObjectWithBackReferences interface [Windows Shell],RemoveBackReferences method, IObjectWithBackReferences.RemoveBackReferences, IObjectWithBackReferences::RemoveBackReferences, RemoveBackReferences, RemoveBackReferences method [Windows Shell], RemoveBackReferences method [Windows Shell],IObjectWithBackReferences interface, _shell_IObjectWithBackReferences_RemoveBackReferences, shell.IObjectWithBackReferences_RemoveBackReferences, shobjidl_core/IObjectWithBackReferences::RemoveBackReferences
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IObjectWithBackReferences.RemoveBackReferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithBackReferences::RemoveBackReferences


## -description


Removes all back references held by an object.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used for all tasks associated with freeing/releasing back references held
    by an object, and may prepare an object for reuse.



