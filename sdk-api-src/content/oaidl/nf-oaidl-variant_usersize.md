---
UID: NF:oaidl.VARIANT_UserSize
title: VARIANT_UserSize function
author: windows-driver-content
description: Calculates the wire size of the VARIANT object, and gets its handle and data.
old-location: automat\variant_usersize.htm
old-project: automat
ms.assetid: 64dc64e5-3de3-4133-835c-b832f5bb20ae
ms.author: windowsdriverdev
ms.date: 5/4/2018
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	VARIANT_UserSize
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VARIANT_UserSize function


## -description


Calculates the wire size of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> object, and gets its handle and data.


## -parameters




### -param

TBD




#### - Offset [in]

The current buffer offset where the object will be marshaled. The method has to account for any padding needed for the object to be properly aligned when it will be marshaled to the buffer.


#### - pFlags [in]

The data used by RPC.


#### - pVariant [in]

The object.


## -returns



The value obtained from the returned <b>HRESULT</b> value is <b>S_OK</b>.



