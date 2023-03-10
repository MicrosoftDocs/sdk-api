---
UID: NF:shobjidl_core.IEnumObjects.Skip
title: IEnumObjects::Skip (shobjidl_core.h)
description: Skips a specified number of objects.
helpviewer_keywords: ["IEnumObjects interface [Windows Shell]","Skip method","IEnumObjects.Skip","IEnumObjects::Skip","Skip","Skip method [Windows Shell]","Skip method [Windows Shell]","IEnumObjects interface","_shell_IEnumObjects_Skip","shell.IEnumObjects_Skip","shobjidl_core/IEnumObjects::Skip"]
old-location: shell\IEnumObjects_Skip.htm
tech.root: shell
ms.assetid: 227be42b-c821-40f4-8bcb-9990d1ceefeb
ms.date: 12/05/2018
ms.keywords: IEnumObjects interface [Windows Shell],Skip method, IEnumObjects.Skip, IEnumObjects::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumObjects interface, _shell_IEnumObjects_Skip, shell.IEnumObjects_Skip, shobjidl_core/IEnumObjects::Skip
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumObjects::Skip
 - shobjidl_core/IEnumObjects::Skip
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
 - IEnumObjects.Skip
---

# IEnumObjects::Skip


## -description

Skips a specified number of objects.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of objects to skip.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Enumeration index is advanced by the number of items skipped.

