---
UID: NF:shlobj_core.INamedPropertyBag.WritePropertyNPB
title: INamedPropertyBag::WritePropertyNPB (shlobj_core.h)
description: Saves a property to the named property bag.
helpviewer_keywords: ["INamedPropertyBag interface [Windows Shell]","WritePropertyNPB method","INamedPropertyBag.WritePropertyNPB","INamedPropertyBag::WritePropertyNPB","WritePropertyNPB","WritePropertyNPB method [Windows Shell]","WritePropertyNPB method [Windows Shell]","INamedPropertyBag interface","_shell_INamedPropertyBag_WritePropertyNPB","shell.INamedPropertyBag_WritePropertyNPB","shlobj_core/INamedPropertyBag::WritePropertyNPB"]
old-location: shell\INamedPropertyBag_WritePropertyNPB.htm
tech.root: shell
ms.assetid: f91764ee-85eb-47ec-b983-49ec410b8c2c
ms.date: 12/05/2018
ms.keywords: INamedPropertyBag interface [Windows Shell],WritePropertyNPB method, INamedPropertyBag.WritePropertyNPB, INamedPropertyBag::WritePropertyNPB, WritePropertyNPB, WritePropertyNPB method [Windows Shell], WritePropertyNPB method [Windows Shell],INamedPropertyBag interface, _shell_INamedPropertyBag_WritePropertyNPB, shell.INamedPropertyBag_WritePropertyNPB, shlobj_core/INamedPropertyBag::WritePropertyNPB
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shdocvw.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INamedPropertyBag::WritePropertyNPB
 - shlobj_core/INamedPropertyBag::WritePropertyNPB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - INamedPropertyBag.WritePropertyNPB
---

# INamedPropertyBag::WritePropertyNPB


## -description

Saves a property to the named property bag.

## -parameters

### -param pszBagname [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property bag.

### -param pszPropName [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property to write.

### -param pVar [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A pointer to a <b>VARIANT</b> that holds the new property value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.