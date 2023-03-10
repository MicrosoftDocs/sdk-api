---
UID: NF:shlobj_core.INamedPropertyBag.RemovePropertyNPB
title: INamedPropertyBag::RemovePropertyNPB (shlobj_core.h)
description: Removes a property from a named property bag.
helpviewer_keywords: ["INamedPropertyBag interface [Windows Shell]","RemovePropertyNPB method","INamedPropertyBag.RemovePropertyNPB","INamedPropertyBag::RemovePropertyNPB","RemovePropertyNPB","RemovePropertyNPB method [Windows Shell]","RemovePropertyNPB method [Windows Shell]","INamedPropertyBag interface","_shell_INamedPropertyBag_RemovePropertyNPB","shell.INamedPropertyBag_RemovePropertyNPB","shlobj_core/INamedPropertyBag::RemovePropertyNPB"]
old-location: shell\INamedPropertyBag_RemovePropertyNPB.htm
tech.root: shell
ms.assetid: 632bab32-c546-4f8f-b064-877e853c215c
ms.date: 12/05/2018
ms.keywords: INamedPropertyBag interface [Windows Shell],RemovePropertyNPB method, INamedPropertyBag.RemovePropertyNPB, INamedPropertyBag::RemovePropertyNPB, RemovePropertyNPB, RemovePropertyNPB method [Windows Shell], RemovePropertyNPB method [Windows Shell],INamedPropertyBag interface, _shell_INamedPropertyBag_RemovePropertyNPB, shell.INamedPropertyBag_RemovePropertyNPB, shlobj_core/INamedPropertyBag::RemovePropertyNPB
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shlobj.idl
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
 - INamedPropertyBag::RemovePropertyNPB
 - shlobj_core/INamedPropertyBag::RemovePropertyNPB
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
 - INamedPropertyBag.RemovePropertyNPB
---

# INamedPropertyBag::RemovePropertyNPB


## -description

Removes a property from a named property bag.

## -parameters

### -param pszBagname [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property bag from which a property is to be removed.

### -param pszPropName [in]

Type: <b>PCWSTR</b>

A pointer to a string that contains the name of the property to remove.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

