---
UID: NF:shobjidl_core.IEnumExtraSearch.Next
title: IEnumExtraSearch::Next (shobjidl_core.h)
description: Used to request information on one or more search objects.
helpviewer_keywords: ["IEnumExtraSearch interface [Windows Shell]","Next method","IEnumExtraSearch.Next","IEnumExtraSearch::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumExtraSearch interface","_win32_IEnumExtraSearch_Next","shell.IEnumExtraSearch_Next","shobjidl_core/IEnumExtraSearch::Next"]
old-location: shell\IEnumExtraSearch_Next.htm
tech.root: shell
ms.assetid: 915f1cd5-5429-4080-8357-753dd1744d93
ms.date: 12/05/2018
ms.keywords: IEnumExtraSearch interface [Windows Shell],Next method, IEnumExtraSearch.Next, IEnumExtraSearch::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumExtraSearch interface, _win32_IEnumExtraSearch_Next, shell.IEnumExtraSearch_Next, shobjidl_core/IEnumExtraSearch::Next
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IEnumExtraSearch::Next
 - shobjidl_core/IEnumExtraSearch::Next
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
 - IEnumExtraSearch.Next
---

# IEnumExtraSearch::Next


## -description

Used to request information on one or more search objects.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The number of search objects to be enumerated, starting from the current object. If <i>celt</i> is too large, the method should stop and return the actual number of search objects in <i>pceltFetched</i>.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch">EXTRASEARCH</a>*</b>

A pointer to an array of <i>pceltFetched</i> <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch">EXTRASEARCH</a> structures containing information on the enumerated objects.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

The number of objects actually enumerated. This may be less than <i>celt</i>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.