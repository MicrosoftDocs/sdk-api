---
UID: NF:oaidl.VARIANT_UserSize64
title: VARIANT_UserSize64 function (oaidl.h)
description: Calculates the wire size of the VARIANT object, and gets its handle and data. (VARIANT_UserSize64)
helpviewer_keywords: ["VARIANT_UserSize64","VARIANT_UserSize64 function [Automation]","automat.variant_usersize64","oaidl/VARIANT_UserSize64"]
old-location: automat\variant_usersize64.htm
tech.root: automat
ms.assetid: a6ae00a6-f126-4550-ae46-96c5ba1aee35
ms.date: 12/05/2018
ms.keywords: VARIANT_UserSize64, VARIANT_UserSize64 function [Automation], automat.variant_usersize64, oaidl/VARIANT_UserSize64
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
 - VARIANT_UserSize64
 - oaidl/VARIANT_UserSize64
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
 - VARIANT_UserSize64
---

# VARIANT_UserSize64 function


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
