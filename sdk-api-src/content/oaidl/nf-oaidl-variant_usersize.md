---
UID: NF:oaidl.VARIANT_UserSize
title: VARIANT_UserSize function
author: windows-sdk-content
description: Calculates the wire size of the VARIANT object, and gets its handle and data.
old-location: automat\variant_usersize.htm
tech.root: automat
ms.assetid: 64dc64e5-3de3-4133-835c-b832f5bb20ae
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VARIANT_UserSize, VARIANT_UserSize function [Automation], _oa96_VARIANT_UserSize, automat.variant_usersize, oaidl/VARIANT_UserSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VARIANT_UserSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VARIANT_UserSize function


## -description


Calculates the wire size of the <a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> object, and gets its handle and data.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - Offset [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the object to be properly aligned when it will be marshaled to the buffer.


#### - [in]

The data used by RPC.


#### - pVariant [in]

The object.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



