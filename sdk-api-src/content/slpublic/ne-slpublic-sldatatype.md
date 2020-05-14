---
UID: NE:slpublic._tagSLDATATYPE
title: SLDATATYPE (slpublic.h)
description: Specifies the data type of the buffer returned by the SLGetWindowsInformation function.helpviewer_keywords: ["SLDATATYPE","SLDATATYPE enumeration [Security]","SL_DATA_BINARY","SL_DATA_DWORD","SL_DATA_MULTI_SZ","SL_DATA_NONE","SL_DATA_SUM","SL_DATA_SZ","security.sldatatype","slpublic/SLDATATYPE","slpublic/SL_DATA_BINARY","slpublic/SL_DATA_DWORD","slpublic/SL_DATA_MULTI_SZ","slpublic/SL_DATA_NONE","slpublic/SL_DATA_SUM","slpublic/SL_DATA_SZ"]
old-location: security\sldatatype.htm
tech.root: SecSLApi
ms.assetid: 245e79de-4823-4af9-926a-088e263cc802
ms.date: 12/05/2018
ms.keywords: SLDATATYPE, SLDATATYPE enumeration [Security], SL_DATA_BINARY, SL_DATA_DWORD, SL_DATA_MULTI_SZ, SL_DATA_NONE, SL_DATA_SUM, SL_DATA_SZ, security.sldatatype, slpublic/SLDATATYPE, slpublic/SL_DATA_BINARY, slpublic/SL_DATA_DWORD, slpublic/SL_DATA_MULTI_SZ, slpublic/SL_DATA_NONE, slpublic/SL_DATA_SUM, slpublic/SL_DATA_SZ
f1_keywords:
- slpublic/SLDATATYPE
dev_langs:
- c++
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Slpublic.h
api_name:
- SLDATATYPE
targetos: Windows
req.typenames: SLDATATYPE
req.redist: 
ms.custom: 19H1
---

# SLDATATYPE enumeration


## -description


Specifies the data type of the buffer returned by the <a href="https://docs.microsoft.com/windows/desktop/api/slpublic/nf-slpublic-slgetwindowsinformation">SLGetWindowsInformation</a> function.


## -enum-fields




### -field SL_DATA_NONE

The buffer has no data type.


### -field SL_DATA_SZ

The buffer contains a null-terminated Unicode string.


### -field SL_DATA_DWORD

The buffer contains a <b>DWORD</b> value.


### -field SL_DATA_BINARY

The buffer contains a binary value.


### -field SL_DATA_MULTI_SZ

The buffer contains multiple null-terminated Unicode strings.


### -field SL_DATA_SUM

The buffer contains a sum.

