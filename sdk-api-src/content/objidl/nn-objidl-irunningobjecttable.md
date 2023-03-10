---
UID: NN:objidl.IRunningObjectTable
title: IRunningObjectTable (objidl.h)
description: Manages access to the running object table (ROT), a globally accessible look-up table on each workstation.
helpviewer_keywords: ["IRunningObjectTable","IRunningObjectTable interface [COM]","IRunningObjectTable interface [COM]","described","_com_irunningobjecttable","com.irunningobjecttable","objidl/IRunningObjectTable"]
old-location: com\irunningobjecttable.htm
tech.root: com
ms.assetid: ff89bcb5-df6d-4325-b0e8-613217a68f42
ms.date: 12/05/2018
ms.keywords: IRunningObjectTable, IRunningObjectTable interface [COM], IRunningObjectTable interface [COM],described, _com_irunningobjecttable, com.irunningobjecttable, objidl/IRunningObjectTable
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IRunningObjectTable
 - objidl/IRunningObjectTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IRunningObjectTable
---

# IRunningObjectTable interface


## -description

Manages access to the running object table (ROT), a globally accessible look-up table on each workstation. A workstation's ROT keeps track of those objects that can be identified by a moniker and that are currently running on the workstation. When a client tries to bind a moniker to an object, the moniker checks the ROT to see if the object is already running; this allows the moniker to bind to the current instance instead of loading a new one.

## -inheritance

The <b>IRunningObjectTable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRunningObjectTable</b> also has these types of members:

## -remarks

The ROT contains entries of the following form: (<i>pmkObjectName</i>, <i>pUnkObject</i>).

The <i>pmkObjectName</i> element is a pointer to the moniker that identifies the running object. The <i>pUnkObject</i> element is a pointer to the running object itself. During the binding process, monikers consult the <i>pmkObjectName</i> entries in the ROT to see whether an object is already running.

Objects that can be named by monikers must be registered with the ROT when they are loaded and their registration must be revoked when they are no longer running.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-getrunningobjecttable">GetRunningObjectTable</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getrunningobjecttable">IBindCtx::GetRunningObjectTable</a>



<a href="/windows/desktop/api/objidl/nn-objidl-irotdata">IROTData</a>
