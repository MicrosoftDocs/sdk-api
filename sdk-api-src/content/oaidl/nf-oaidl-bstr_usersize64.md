---
UID: NF:oaidl.BSTR_UserSize64
title: BSTR_UserSize64 function (oaidl.h)
description: Calculates the wire size of the BSTR object, and gets its handle and data. (BSTR_UserSize64)
helpviewer_keywords: ["BSTR_UserSize64","BSTR_UserSize64 function [Automation]","automat.bstr_usersize64","oaidl/BSTR_UserSize64"]
old-location: automat\bstr_usersize64.htm
tech.root: automat
ms.assetid: 56ba0992-b5df-419d-b531-ea974413a7b0
ms.date: 12/05/2018
ms.keywords: BSTR_UserSize64, BSTR_UserSize64 function [Automation], automat.bstr_usersize64, oaidl/BSTR_UserSize64
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - BSTR_UserSize64
 - oaidl/BSTR_UserSize64
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
 - BSTR_UserSize64
---

# BSTR_UserSize64 function


## -description

Calculates the wire size of the <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> object, and gets its handle and data.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> object to be properly aligned when it will be marshaled to the buffer.

### -param unnamedParam3 [in]

The object.

## -returns

The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.
