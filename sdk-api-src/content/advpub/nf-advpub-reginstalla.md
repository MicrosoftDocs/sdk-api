---
UID: NF:advpub.RegInstallA
title: RegInstallA function
author: windows-sdk-content
description: Updates the string registry values in the provided table.
old-location: winprog\reginstalla.htm
tech.root: devnotes
ms.assetid: 53BE8B69-2028-42EB-9A45-6CE776A7B9A6
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: RegInstallA, RegInstallA function [Windows API], advpub/RegInstallA, winprog.reginstalla
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: advpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advpack.lib
req.dll: Advpack.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - advpack.dll
api_name:
 - RegInstallA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegInstallA function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Updates the string registry values in the provided table.


## -parameters




### -param hmod

The module containing the values to be updated.


### -param pszSection

The sections containing the values to be updated.


### -param pstTable

The table of values to be updated.


## -returns



Returns S_OK on success. Returns E_FAIL on failure.



