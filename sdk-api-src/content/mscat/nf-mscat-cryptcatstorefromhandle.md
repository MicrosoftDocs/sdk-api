---
UID: NF:mscat.CryptCATStoreFromHandle
title: CryptCATStoreFromHandle function
author: windows-sdk-content
description: Retrieves a CRYPTCATSTORE structure from a catalog handle.
old-location: security\cryptcatstorefromhandle.htm
tech.root: seccrypto
ms.assetid: ce4fe972-0ed5-4b18-8ec5-9883af326335
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CryptCATStoreFromHandle, CryptCATStoreFromHandle function [Security], mscat/CryptCATStoreFromHandle, security.cryptcatstorefromhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATStoreFromHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATStoreFromHandle function


## -description


<p class="CCE_Message">[The  <b>CryptCATStoreFromHandle</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATStoreFromHandle</b> function retrieves a <a href="https://msdn.microsoft.com/65a15797-453c-4f47-8ea1-c92e616b50aa">CRYPTCATSTORE</a> structure from a catalog handle.


## -parameters




### -param hCatalog [in]

A handle to the catalog obtained from the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> or <a href="https://msdn.microsoft.com/e9aedc2d-9492-4ed7-9f2d-891997f85f6f">CryptCATHandleFromStore</a> function.


## -returns



A pointer to a <a href="https://msdn.microsoft.com/65a15797-453c-4f47-8ea1-c92e616b50aa">CRYPTCATSTORE</a> structure that contains the catalog store. The caller must not free this pointer or any of its members.



