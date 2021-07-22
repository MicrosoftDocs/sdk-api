---
UID: NN:propsys.IPropertySystem
title: IPropertySystem (propsys.h)
description: Exposes methods that get property descriptions, register and unregister property schemas, enumerate property descriptions, and format property values in a type-strict way.
helpviewer_keywords: ["IPropertySystem","IPropertySystem interface [Windows Properties]","IPropertySystem interface [Windows Properties]","described","properties.IPropertySystem","propsys/IPropertySystem","shell.IPropertySystem","shell_IPropertySystem"]
old-location: properties\IPropertySystem.htm
tech.root: properties
ms.assetid: 9ead94d9-4d4e-44c6-8c53-11c4c4ee2fb2
ms.date: 12/05/2018
ms.keywords: IPropertySystem, IPropertySystem interface [Windows Properties], IPropertySystem interface [Windows Properties],described, properties.IPropertySystem, propsys/IPropertySystem, shell.IPropertySystem, shell_IPropertySystem
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IPropertySystem
 - propsys/IPropertySystem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertySystem
---

# IPropertySystem interface


## -description

Exposes methods that get property descriptions, register and unregister property schemas, enumerate property descriptions, and format property values in a type-strict way.

## -inheritance

The <b>IPropertySystem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertySystem</b> also has these types of members:

## -remarks

Many of the exported APIs (such as <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a>) are simply wrappers around the <a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a> methods. If your code calls a lot of these helper APIs in sequence, it may be worthwhile to instantiate a single <b>IPropertySystem</b> object, and call the methods directly, rather than calling the helper APIs. (To improve the performance, the helper APIs do obtain a cached instance of the <b>IPropertySystem</b> object.)
