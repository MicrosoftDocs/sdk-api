---
UID: NF:mscat.CryptCATHandleFromStore
title: CryptCATHandleFromStore function
author: windows-sdk-content
description: Retrieves a catalog handle from memory.
old-location: security\cryptcathandlefromstore.htm
old-project: seccrypto
ms.assetid: e9aedc2d-9492-4ed7-9f2d-891997f85f6f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CryptCATHandleFromStore, CryptCATHandleFromStore function [Security], mscat/CryptCATHandleFromStore, security.cryptcathandlefromstore
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATHandleFromStore
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATHandleFromStore function


## -description


<p class="CCE_Message">[The  <b>CryptCATHandleFromStore</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATHandleFromStore</b> function retrieves a catalog handle from memory.


## -parameters




### -param pCatStore [in]

A pointer to a <a href="https://msdn.microsoft.com/65a15797-453c-4f47-8ea1-c92e616b50aa">CRYPTCATSTORE</a> structure that contains the handle to retrieve.


## -returns



A handle to the catalog.



