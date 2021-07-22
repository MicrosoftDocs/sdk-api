---
UID: NN:reconcil.IReconcileInitiator
title: IReconcileInitiator (reconcil.h)
description: Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document. The initiator is responsible for implementing this interface.
helpviewer_keywords: ["IReconcileInitiator","IReconcileInitiator interface [Legacy Windows Environment Features]","IReconcileInitiator interface [Legacy Windows Environment Features]","described","_win32_IReconcileInitiator","lwef.ireconcileinitiator","reconcil/IReconcileInitiator","shell.ireconcileinitiator"]
old-location: lwef\ireconcileinitiator.htm
tech.root: lwef
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
ms.date: 12/05/2018
ms.keywords: IReconcileInitiator, IReconcileInitiator interface [Legacy Windows Environment Features], IReconcileInitiator interface [Legacy Windows Environment Features],described, _win32_IReconcileInitiator, lwef.ireconcileinitiator, reconcil/IReconcileInitiator, shell.ireconcileinitiator
req.header: reconcil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IReconcileInitiator
 - reconcil/IReconcileInitiator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IReconcileInitiator
---

# IReconcileInitiator interface


## -description

Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document. The initiator is responsible for implementing this interface.

## -inheritance

The <b>IReconcileInitiator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IReconcileInitiator</b> also has these types of members:

