---
UID: NF:oaidl.VARIANT_UserSize
title: VARIANT_UserSize function (oaidl.h)
description: Calculates the wire size of the VARIANT object, and gets its handle and data. (VARIANT_UserSize)
helpviewer_keywords: ["VARIANT_UserSize","VARIANT_UserSize function [Automation]","_oa96_VARIANT_UserSize","automat.variant_usersize","oaidl/VARIANT_UserSize"]
old-location: automat\variant_usersize.htm
tech.root: automat
ms.assetid: 64dc64e5-3de3-4133-835c-b832f5bb20ae
ms.date: 12/05/2018
ms.keywords: VARIANT_UserSize, VARIANT_UserSize function [Automation], _oa96_VARIANT_UserSize, automat.variant_usersize, oaidl/VARIANT_UserSize
req.header: oaidl.h
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
 - VARIANT_UserSize
 - oaidl/VARIANT_UserSize
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
 - VARIANT_UserSize
---

# VARIANT_UserSize function


## -description

Calculates the wire size of the <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> object, and gets its handle and data.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the object to be properly aligned when it will be marshaled to the buffer.

### -param unnamedParam3 [in]

The object.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.
