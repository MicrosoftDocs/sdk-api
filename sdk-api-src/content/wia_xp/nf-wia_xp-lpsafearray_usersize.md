---
UID: NF:wia_xp.LPSAFEARRAY_UserSize
title: LPSAFEARRAY_UserSize function (wia_xp.h)
description: Calculates the wire size of the SAFEARRAY object, and gets its handle and data. (LPSAFEARRAY_UserSize)
helpviewer_keywords: ["LPSAFEARRAY_UserSize","LPSAFEARRAY_UserSize function [Automation]","_oa96_LPSAFEARRAY_UserSize","automat.lpsafearray_usersize","wia_xp/LPSAFEARRAY_UserSize"]
old-location: automat\lpsafearray_usersize.htm
tech.root: wia
ms.assetid: 85cb5bc1-5dab-4b50-950e-0d18c403f996
ms.date: 12/05/2018
ms.keywords: LPSAFEARRAY_UserSize, LPSAFEARRAY_UserSize function [Automation], _oa96_LPSAFEARRAY_UserSize, automat.lpsafearray_usersize, wia_xp/LPSAFEARRAY_UserSize
req.header: wia_xp.h
req.include-header: Propidlbase.h
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
 - LPSAFEARRAY_UserSize
 - wia_xp/LPSAFEARRAY_UserSize
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
 - LPSAFEARRAY_UserSize
archived: true
---

# LPSAFEARRAY_UserSize function


## -description

Calculates the wire size of the <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> object, and gets its handle and data.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

Sets the buffer offset so that the <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> object is properly aligned when it is marshaled to the buffer.

### -param unnamedParam3 [in]

The safe array that contains the data to marshal.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.
