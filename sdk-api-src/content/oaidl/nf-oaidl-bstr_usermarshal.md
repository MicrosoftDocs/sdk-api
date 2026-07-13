---
UID: NF:oaidl.BSTR_UserMarshal
title: BSTR_UserMarshal function (oaidl.h)
description: Marshals a BSTR object into the RPC buffer. (BSTR_UserMarshal)
helpviewer_keywords: ["BSTR_UserMarshal","BSTR_UserMarshal function [Automation]","_oa96_BSTR_UserMarshal","automat.bstr_usermarshal","oaidl/BSTR_UserMarshal"]
old-location: automat\bstr_usermarshal.htm
tech.root: automat
ms.assetid: 98825155-1dd3-47c0-928d-484d5bc70927
ms.date: 12/05/2018
ms.keywords: BSTR_UserMarshal, BSTR_UserMarshal function [Automation], _oa96_BSTR_UserMarshal, automat.bstr_usermarshal, oaidl/BSTR_UserMarshal
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
 - BSTR_UserMarshal
 - oaidl/BSTR_UserMarshal
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
 - BSTR_UserMarshal
---

# BSTR_UserMarshal function


## -description

Marshals a <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> object into the RPC buffer.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in, out]

The current buffer. This pointer may or may not be aligned on entry.

### -param unnamedParam3 [in]

The object.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.
