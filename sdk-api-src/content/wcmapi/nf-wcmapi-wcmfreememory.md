---
UID: NF:wcmapi.WcmFreeMemory
title: WcmFreeMemory function (wcmapi.h)
description: Is used to release memory resources allocated by the WCM functions.helpviewer_keywords: ["WcmFreeMemory","WcmFreeMemory function [Windows Connection Manager]","wcm.wcmfreememory","wcmapi/WcmFreeMemory"]
old-location: wcm\wcmfreememory.htm
tech.root: wcm
ms.assetid: 43377f58-9702-472d-874a-898f29b743d8
ms.date: 12/05/2018
ms.keywords: WcmFreeMemory, WcmFreeMemory function [Windows Connection Manager], wcm.wcmfreememory, wcmapi/WcmFreeMemory
f1_keywords:
- wcmapi/WcmFreeMemory
dev_langs:
- c++
req.header: wcmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wcmapi.lib
req.dll: Wcmapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wcmapi.dll
- Ext-MS-Win-networking-wcmapi-l1-1-0.dll
api_name:
- WcmFreeMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WcmFreeMemory function


## -description


The <b>WcmFreeMemory</b> function is used to release memory resources allocated by the WCM functions.


## -parameters




### -param pMemory

Pointer to the memory to be freed.


