---
UID: NF:shobjidl_core.IEnumResources.Skip
title: IEnumResources::Skip (shobjidl_core.h)
description: Skips a specified number of resources.
old-location: shell\IEnumResources_Skip.htm
tech.root: shell
ms.assetid: d3dc94e7-5455-4afb-8743-05c993e1448b
ms.date: 12/05/2018
ms.keywords: IEnumResources interface [Windows Shell],Skip method, IEnumResources.Skip, IEnumResources::Skip, Skip, Skip method [Windows Shell], Skip method [Windows Shell],IEnumResources interface, _shell_IEnumResources_Skip, shell.IEnumResources_Skip, shobjidl_core/IEnumResources::Skip
ms.topic: method
f1_keywords:
- shobjidl_core/IEnumResources.Skip
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IEnumResources.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumResources::Skip


## -description


Skips a specified number of resources.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of resources to skip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



