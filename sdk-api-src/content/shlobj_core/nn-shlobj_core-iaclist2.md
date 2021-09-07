---
UID: NN:shlobj_core.IACList2
title: IACList2 (shlobj_core.h)
description: Extends the IACList interface to enable clients of an autocomplete object to retrieve and set option flags.
helpviewer_keywords: ["IACList2","IACList2 interface [Windows Shell]","IACList2 interface [Windows Shell]","described","_win32_IACList2","shell.IACList2","shlobj_core/IACList2"]
old-location: shell\IACList2.htm
tech.root: shell
ms.assetid: b765c9dd-20e9-428f-877a-aff4fac44664
ms.date: 12/05/2018
ms.keywords: IACList2, IACList2 interface [Windows Shell], IACList2 interface [Windows Shell],described, _win32_IACList2, shell.IACList2, shlobj_core/IACList2
req.header: shlobj_core.h
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IACList2
 - shlobj_core/IACList2
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
 - IACList2
---

# IACList2 interface


## -description

Extends the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist">IACList</a> interface to enable clients of an autocomplete object to retrieve and set option flags.

## -inheritance

The <b>IACList2</b> interface inherits from <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist">IACList</a>. <b>IACList2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist">IACList</a> interface from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>

<a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">Autocompletion</a> clients implement this interface to enable the autocomplete object to retrieve and set options. The options are basically a request that the client generate a list with the names of all the files and subfolders contained by one or more specified folders. The autocomplete object then calls the client's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface to request the strings.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Typically, this interface is not used directly by applications.
