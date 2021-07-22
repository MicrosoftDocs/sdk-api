---
UID: NF:shobjidl_core.IObjectWithBackReferences.RemoveBackReferences
title: IObjectWithBackReferences::RemoveBackReferences (shobjidl_core.h)
description: Removes all back references held by an object.
helpviewer_keywords: ["IObjectWithBackReferences interface [Windows Shell]","RemoveBackReferences method","IObjectWithBackReferences.RemoveBackReferences","IObjectWithBackReferences::RemoveBackReferences","RemoveBackReferences","RemoveBackReferences method [Windows Shell]","RemoveBackReferences method [Windows Shell]","IObjectWithBackReferences interface","_shell_IObjectWithBackReferences_RemoveBackReferences","shell.IObjectWithBackReferences_RemoveBackReferences","shobjidl_core/IObjectWithBackReferences::RemoveBackReferences"]
old-location: shell\IObjectWithBackReferences_RemoveBackReferences.htm
tech.root: shell
ms.assetid: 642fe793-974f-48e5-90a2-de6ba7a5b033
ms.date: 12/05/2018
ms.keywords: IObjectWithBackReferences interface [Windows Shell],RemoveBackReferences method, IObjectWithBackReferences.RemoveBackReferences, IObjectWithBackReferences::RemoveBackReferences, RemoveBackReferences, RemoveBackReferences method [Windows Shell], RemoveBackReferences method [Windows Shell],IObjectWithBackReferences interface, _shell_IObjectWithBackReferences_RemoveBackReferences, shell.IObjectWithBackReferences_RemoveBackReferences, shobjidl_core/IObjectWithBackReferences::RemoveBackReferences
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectWithBackReferences::RemoveBackReferences
 - shobjidl_core/IObjectWithBackReferences::RemoveBackReferences
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
 - IObjectWithBackReferences.RemoveBackReferences
---

# IObjectWithBackReferences::RemoveBackReferences


## -description

Removes all back references held by an object.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used for all tasks associated with freeing/releasing back references held
    by an object, and may prepare an object for reuse.

