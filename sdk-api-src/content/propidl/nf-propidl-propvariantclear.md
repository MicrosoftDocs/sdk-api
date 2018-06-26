---
UID: NF:propidl.PropVariantClear
title: PropVariantClear function
author: windows-sdk-content
description: Clears a PROPVARIANT structure.
old-location: properties\PropVariantClear.htm
old-project: properties
ms.assetid: 68b00e4b-39d3-49e3-8a0d-032edcb23b06
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantClear, PropVariantClear function [Windows Properties], _shell_PropVariantClear, properties.PropVariantClear, propidl/PropVariantClear, shell.PropVariantClear
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps | UWP apps]
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
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - PropVariantClear
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantClear function


## -description


Clears a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param pvar [in, out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure to clear. When this function successfully returns, the <b>PROPVARIANT</b> is zeroed and the type is set to VT_EMPTY.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



