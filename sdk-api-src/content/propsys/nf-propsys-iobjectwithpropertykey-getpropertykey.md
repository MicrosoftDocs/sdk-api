---
UID: NF:propsys.IObjectWithPropertyKey.GetPropertyKey
title: IObjectWithPropertyKey::GetPropertyKey (propsys.h)
description: Gets the property key.
helpviewer_keywords: ["GetPropertyKey","GetPropertyKey method [Windows Shell]","GetPropertyKey method [Windows Shell]","IObjectWithPropertyKey interface","IObjectWithPropertyKey interface [Windows Shell]","GetPropertyKey method","IObjectWithPropertyKey.GetPropertyKey","IObjectWithPropertyKey::GetPropertyKey","_shell_IObjectWithPropertyKey_GetPropertyKey","propsys/IObjectWithPropertyKey::GetPropertyKey","shell.IObjectWithPropertyKey_GetPropertyKey"]
old-location: shell\IObjectWithPropertyKey_GetPropertyKey.htm
tech.root: shell
ms.assetid: e864f1d2-b83e-4196-8cd4-a7c7fdcddfec
ms.date: 12/05/2018
ms.keywords: GetPropertyKey, GetPropertyKey method [Windows Shell], GetPropertyKey method [Windows Shell],IObjectWithPropertyKey interface, IObjectWithPropertyKey interface [Windows Shell],GetPropertyKey method, IObjectWithPropertyKey.GetPropertyKey, IObjectWithPropertyKey::GetPropertyKey, _shell_IObjectWithPropertyKey_GetPropertyKey, propsys/IObjectWithPropertyKey::GetPropertyKey, shell.IObjectWithPropertyKey_GetPropertyKey
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectWithPropertyKey::GetPropertyKey
 - propsys/IObjectWithPropertyKey::GetPropertyKey
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
 - IObjectWithPropertyKey.GetPropertyKey
---

# IObjectWithPropertyKey::GetPropertyKey


## -description

Gets the property key.

## -parameters

### -param pkey [out]

Type: <b><a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

When this returns, contains the property key.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.