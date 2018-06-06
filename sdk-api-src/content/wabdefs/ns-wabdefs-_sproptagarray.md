---
UID: NS:wabdefs._SPropTagArray
title: "_SPropTagArray"
author: windows-sdk-content
description: Do not use. Contains an array of property tags.
old-location: wab\_wab_SPropTagArray.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\sproptagarray.htm
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPSPropTagArray, SPropTagArray, SPropTagArray structure [Windows Address Book], _SPropTagArray, _wab_SPropTagArray, wab._wab_SPropTagArray, wabdefs/SPropTagArray"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SPropTagArray, *LPSPropTagArray
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wabdefs.h
api_name:
 - SPropTagArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _SPropTagArray structure


## -description


Do not use. Contains an array of property tags.


## -struct-fields




### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of property tags in the array indicated by the <b>aulPropTag</b> member.


### -field aulPropTag

Type: <b>ULONG[MAPI_DIM]</b>

Array of variables of type <b>ULONG</b> that specify the property tags.

