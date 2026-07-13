---
UID: NL:shidfact.CItemIDFactory
title: CItemIDFactory (shidfact.h)
description: Exposes methods for interacting with Shell data sources.
helpviewer_keywords: ["CItemIDFactory","CItemIDFactory class [Windows Shell]","CItemIDFactory class [Windows Shell]","described","shell.citemidfactory","shidfact/CItemIDFactory"]
old-location: shell\citemidfactory.htm
tech.root: shell
ms.assetid: 8C13F1AF-3328-40B8-B5F8-6CDF753A7FA7
ms.date: 12/05/2018
ms.keywords: CItemIDFactory, CItemIDFactory class [Windows Shell], CItemIDFactory class [Windows Shell],described, shell.citemidfactory, shidfact/CItemIDFactory
req.header: shidfact.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - CItemIDFactory
 - shidfact/CItemIDFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shidfact.h
api_name:
 - CItemIDFactory
---

# CItemIDFactory class


## -description

Exposes methods for interacting with Shell data sources.

## -inheritance

The <b>CItemIDFactory</b> class inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder">IDelegateFolder</a>. <b>CItemIDFactory</b> also has these types of members:

## -remarks

it is recommended that all data sources use this as it manages an important issue of security when dealing with IDList parsing.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder">IDelegateFolder</a>
