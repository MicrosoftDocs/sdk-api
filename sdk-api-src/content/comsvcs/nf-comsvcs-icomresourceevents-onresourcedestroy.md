---
UID: NF:comsvcs.IComResourceEvents.OnResourceDestroy
title: IComResourceEvents::OnResourceDestroy (comsvcs.h)
description: Generated when a resource is destroyed.helpviewer_keywords: ["IComResourceEvents interface [COM+]","OnResourceDestroy method","IComResourceEvents.OnResourceDestroy","IComResourceEvents::OnResourceDestroy","OnResourceDestroy","OnResourceDestroy method [COM+]","OnResourceDestroy method [COM+]","IComResourceEvents interface","_dtc_IComResourceEvents_OnResourceDestroy","comsvcs/IComResourceEvents::OnResourceDestroy","cos.icomresourceevents_onresourcedestroy"]
old-location: cos\icomresourceevents_onresourcedestroy.htm
tech.root: cossdk
ms.assetid: cc934b47-8031-4dab-ae00-6389f54749b8
ms.date: 12/05/2018
ms.keywords: IComResourceEvents interface [COM+],OnResourceDestroy method, IComResourceEvents.OnResourceDestroy, IComResourceEvents::OnResourceDestroy, OnResourceDestroy, OnResourceDestroy method [COM+], OnResourceDestroy method [COM+],IComResourceEvents interface, _dtc_IComResourceEvents_OnResourceDestroy, comsvcs/IComResourceEvents::OnResourceDestroy, cos.icomresourceevents_onresourcedestroy
f1_keywords:
- comsvcs/IComResourceEvents.OnResourceDestroy
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IComResourceEvents.OnResourceDestroy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComResourceEvents::OnResourceDestroy


## -description


Generated when a resource is destroyed.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.


### -param ObjectID [in]

The just-in-time activated object.


### -param hr [in]

The result from resource dispensers destroy call.


### -param pszType [in]

A description of the resource.


### -param resId [in]

The unique identifier of the resource.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomresourceevents">IComResourceEvents</a>
 

 

