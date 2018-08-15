---
UID: NE:slpublic._tagSLDATATYPE
title: "_tagSLDATATYPE"
author: windows-sdk-content
description: Specifies the data type of the buffer returned by the SLGetWindowsInformation function.
old-location: security\sldatatype.htm
old-project: secslapi
ms.assetid: 245e79de-4823-4af9-926a-088e263cc802
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SLDATATYPE, SLDATATYPE enumeration [Security], SL_DATA_BINARY, SL_DATA_DWORD, SL_DATA_MULTI_SZ, SL_DATA_NONE, SL_DATA_SUM, SL_DATA_SZ, _tagSLDATATYPE, security.sldatatype, slpublic/SLDATATYPE, slpublic/SL_DATA_BINARY, slpublic/SL_DATA_DWORD, slpublic/SL_DATA_MULTI_SZ, slpublic/SL_DATA_NONE, slpublic/SL_DATA_SUM, slpublic/SL_DATA_SZ
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: slpublic.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SLDATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Slpublic.h
api_name:
 - SLDATATYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _tagSLDATATYPE enumeration


## -description


Specifies the data type of the buffer returned by the <a href="https://msdn.microsoft.com/007b3f3a-c320-4bbc-ab5c-746b513cb815">SLGetWindowsInformation</a> function.


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

