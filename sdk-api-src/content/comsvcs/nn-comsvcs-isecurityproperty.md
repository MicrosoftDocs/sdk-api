---
UID: NN:comsvcs.ISecurityProperty
title: ISecurityProperty (comsvcs.h)
description: Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the ISecurityCallContext interface.
helpviewer_keywords: ["ISecurityProperty","ISecurityProperty interface [COM+]","ISecurityProperty interface [COM+]","described","_cos_ISecurityProperty","comsvcs/ISecurityProperty","cos.isecurityproperty"]
old-location: cos\isecurityproperty.htm
tech.root: cos
ms.assetid: 116715a5-a3e1-48aa-b155-107ea330b7ee
ms.date: 12/05/2018
ms.keywords: ISecurityProperty, ISecurityProperty interface [COM+], ISecurityProperty interface [COM+],described, _cos_ISecurityProperty, comsvcs/ISecurityProperty, cos.isecurityproperty
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
 - ISecurityProperty
 - comsvcs/ISecurityProperty
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
 - ISecurityProperty
---

# ISecurityProperty interface


## -description

Determines the security identifier of the current object's original caller or direct caller. However, the preferred way to get information about an object's callers is to use the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a> interface.

## -inheritance

The <b>ISecurityProperty</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISecurityProperty</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="/windows/desktop/cossdk/programmatic-component-security">Programmatic Component Security</a>
