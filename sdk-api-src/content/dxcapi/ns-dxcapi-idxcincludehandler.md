---
UID: NS:dxcapi.IDxcIncludeHandler
tech.root: direct3dhlsl
title: IDxcIncludeHandler
ms.date: 04/05/2023
targetos: Windows
description: Interface for handling include directives. To customize the handling of include directives, you can provide an implementation of this interface.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - IDxcIncludeHandler
f1_keywords:
 - IDxcIncludeHandler
 - dxcapi/IDxcIncludeHandler
dev_langs:
 - c++
helpviewer_keywords:
 - IDxcIncludeHandler
---

## -description

Interface for handling include directives. To customize the handling of include directives, you can provide an implementation of this interface.

To create a default implementation that reads include files from the filesystem, call [IDxcUtils::CreateDefaultIncludeHandler](./nf-dxcapi-idxcutils-createdefaultincludehandler.md).

## -remarks

## -see-also
