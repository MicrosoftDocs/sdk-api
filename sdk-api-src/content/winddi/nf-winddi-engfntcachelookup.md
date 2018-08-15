---
UID: NF:winddi.EngFntCacheLookUp
title: EngFntCacheLookUp function
author: windows-sdk-content
description: The EngFntCacheLookUp function retrieves the address of cached font file data.
old-location: display\engfntcachelookup.htm
old-project: display
ms.assetid: daf93826-fdcb-4c9d-ade6-ad4f0ef40ff5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngFntCacheLookUp, EngFntCacheLookUp function [Display Devices], display.engfntcachelookup, gdifncs_2fee1e8e-2cb5-4088-b0aa-f697689fe56f.xml, winddi/EngFntCacheLookUp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: This function is available in Windows XP and later.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngFntCacheLookUp
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFntCacheLookUp function


## -description


The <b>EngFntCacheLookUp</b> function retrieves the address of cached font file data.


## -parameters




### -param FastCheckSum [in]

Specifies the checksum for the font.


### -param pulSize [out]

Pointer to a memory location that receives the size, in bytes, of the data.


## -returns



On success, this function returns a pointer to the cached data. Otherwise, it returns <b>NULL</b>.




## -remarks



The font engine calls the font driver's <a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a> entry point when a font file is first loaded. It is in this call that the font driver receives a value for <i>FastCheckSum</i>, which it subsequently uses when it calls this function.




## -see-also




<a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/fd0765e0-decd-46fb-872e-4c750713abe6">EngFntCacheAlloc</a>



<a href="https://msdn.microsoft.com/27a44779-64df-4a3f-b8b8-9e0417010969">EngFntCacheFault</a>
 

 

