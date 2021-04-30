---
UID: NF:comsvcs.IMtsEvents.get_PackageName
title: IMtsEvents::get_PackageName (comsvcs.h)
description: Retrieves the name of the package in which the instance of the object that implements the IMtsEvents interface is running.
helpviewer_keywords: ["IMtsEvents interface [COM+]","get_PackageName method","IMtsEvents.get_PackageName","IMtsEvents::get_PackageName","_dtc_IMtsEvents_PackageName","comsvcs/IMtsEvents::get_PackageName","cos.imtsevents_get_packagename","get_PackageName","get_PackageName method [COM+]","get_PackageName method [COM+]","IMtsEvents interface"]
old-location: cos\imtsevents_get_packagename.htm
tech.root: cos
ms.assetid: 0b23828f-cadc-472d-9186-0712e0120b60
ms.date: 12/05/2018
ms.keywords: IMtsEvents interface [COM+],get_PackageName method, IMtsEvents.get_PackageName, IMtsEvents::get_PackageName, _dtc_IMtsEvents_PackageName, comsvcs/IMtsEvents::get_PackageName, cos.imtsevents_get_packagename, get_PackageName, get_PackageName method [COM+], get_PackageName method [COM+],IMtsEvents interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMtsEvents::get_PackageName
 - comsvcs/IMtsEvents::get_PackageName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsEvents.get_PackageName
---

# IMtsEvents::get_PackageName


## -description

Retrieves the name of the package in which the instance of the object that implements the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a> interface is running.

## -parameters

### -param pVal [out]

A pointer to the package name string.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>