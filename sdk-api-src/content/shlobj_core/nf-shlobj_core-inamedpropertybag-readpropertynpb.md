---
UID: NF:shlobj_core.INamedPropertyBag.ReadPropertyNPB
title: INamedPropertyBag::ReadPropertyNPB (shlobj_core.h)
description: Causes a property to be read from the named property bag.
helpviewer_keywords: ["INamedPropertyBag interface [Windows Shell]","ReadPropertyNPB method","INamedPropertyBag.ReadPropertyNPB","INamedPropertyBag::ReadPropertyNPB","ReadPropertyNPB","ReadPropertyNPB method [Windows Shell]","ReadPropertyNPB method [Windows Shell]","INamedPropertyBag interface","_shell_INamedPropertyBag_ReadPropertyNPB","shell.INamedPropertyBag_ReadPropertyNPB","shlobj_core/INamedPropertyBag::ReadPropertyNPB"]
old-location: shell\INamedPropertyBag_ReadPropertyNPB.htm
tech.root: shell
ms.assetid: 7080edeb-4908-4b0a-9416-9b301c54bb4c
ms.date: 12/05/2018
ms.keywords: INamedPropertyBag interface [Windows Shell],ReadPropertyNPB method, INamedPropertyBag.ReadPropertyNPB, INamedPropertyBag::ReadPropertyNPB, ReadPropertyNPB, ReadPropertyNPB method [Windows Shell], ReadPropertyNPB method [Windows Shell],INamedPropertyBag interface, _shell_INamedPropertyBag_ReadPropertyNPB, shell.INamedPropertyBag_ReadPropertyNPB, shlobj_core/INamedPropertyBag::ReadPropertyNPB
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
 - INamedPropertyBag::ReadPropertyNPB
 - shlobj_core/INamedPropertyBag::ReadPropertyNPB
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
 - INamedPropertyBag.ReadPropertyNPB
---

# INamedPropertyBag::ReadPropertyNPB


## -description

Causes a property to be read from the named property bag.

## -parameters

### -param pszBagname [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property bag.

### -param pszPropName [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property to be read.

### -param pVar [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

The address of a <b>VARIANT</b> that, when this method returns successfully, receives the property value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.