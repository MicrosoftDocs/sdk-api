---
UID: NF:oleauto.SafeArrayCreateVectorEx
title: SafeArrayCreateVectorEx function (oleauto.h)
description: Creates and returns a one-dimensional safe array of the specified VARTYPE and bounds.
helpviewer_keywords: ["SafeArrayCreateVectorEx","SafeArrayCreateVectorEx function [Automation]","_oa96_SafeArrayCreateVectorEx","automat.safearraycreatevectorex","oleauto/SafeArrayCreateVectorEx"]
old-location: automat\safearraycreatevectorex.htm
tech.root: automat
ms.assetid: 45f2ba42-4189-42eb-9f6c-772198296906
ms.date: 12/05/2018
ms.keywords: SafeArrayCreateVectorEx, SafeArrayCreateVectorEx function [Automation], _oa96_SafeArrayCreateVectorEx, automat.safearraycreatevectorex, oleauto/SafeArrayCreateVectorEx
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayCreateVectorEx
 - oleauto/SafeArrayCreateVectorEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCreateVectorEx
---

# SafeArrayCreateVectorEx function


## -description

Creates and returns a one-dimensional safe array of the specified VARTYPE and bounds.

## -parameters

### -param vt [in]

The base type of the array (the VARTYPE of each element of the array). The FADF_RECORD flag can be set for VT_RECORD. The FADF_HAVEIID can be set for VT_DISPATCH or VT_UNKNOWN and FADF_HAVEVARTYPE can be set for all other types.

### -param lLbound [in]

The lower bound for the array. This parameter can be negative.

### -param cElements [in]

The number of elements in the array.

### -param pvExtra [in]

The type information of the user-defined type, if you are creating a safe array of user-defined types. If the vt parameter is VT_RECORD, then <i>pvExtra</i> will be a pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-irecordinfo">IRecordInfo</a> describing the record. If the <i>vt</i> parameter is VT_DISPATCH or VT_UNKNOWN, then <i>pvExtra</i> will contain a pointer to a GUID representing the type of interface being passed to the array.

## -returns

A safe array descriptor, or null if the array could not be created.