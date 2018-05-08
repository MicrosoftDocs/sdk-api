---
UID: NF:propsys.IObjectWithPropertyKey.GetPropertyKey
title: IObjectWithPropertyKey::GetPropertyKey
author: windows-driver-content
description: Gets the property key.
old-location: shell\IObjectWithPropertyKey_GetPropertyKey.htm
old-project: shell
ms.assetid: e864f1d2-b83e-4196-8cd4-a7c7fdcddfec
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetPropertyKey, GetPropertyKey method [Windows Shell], GetPropertyKey method [Windows Shell],IObjectWithPropertyKey interface, IObjectWithPropertyKey interface [Windows Shell],GetPropertyKey method, IObjectWithPropertyKey.GetPropertyKey, IObjectWithPropertyKey::GetPropertyKey, _shell_IObjectWithPropertyKey_GetPropertyKey, propsys/IObjectWithPropertyKey::GetPropertyKey, shell.IObjectWithPropertyKey_GetPropertyKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IObjectWithPropertyKey.GetPropertyKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IObjectWithPropertyKey::GetPropertyKey


## -description


Gets the property key.


## -parameters




### -param pkey [out]

Type: <b><a href="https://msdn.microsoft.com/3f5f31af-f040-443b-9045-9761055381ea">PROPERTYKEY</a>*</b>

When this returns, contains the property key.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



