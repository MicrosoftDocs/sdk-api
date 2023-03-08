---
UID: NF:oaidl.BSTR_UserSize
title: BSTR_UserSize function (oaidl.h)
description: Calculates the wire size of the BSTR object, and gets its handle and data. (BSTR_UserSize)
helpviewer_keywords: ["BSTR_UserSize","BSTR_UserSize function [Automation]","_oa96_BSTR_UserSize","automat.bstr_usersize","oaidl/BSTR_UserSize"]
old-location: automat\bstr_usersize.htm
tech.root: automat
ms.assetid: 16c349b4-21e1-45bb-8b24-d299adb36e14
ms.date: 12/05/2018
ms.keywords: BSTR_UserSize, BSTR_UserSize function [Automation], _oa96_BSTR_UserSize, automat.bstr_usersize, oaidl/BSTR_UserSize
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
 - BSTR_UserSize
 - oaidl/BSTR_UserSize
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
 - BSTR_UserSize
---

# BSTR_UserSize function


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
