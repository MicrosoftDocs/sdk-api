---
UID: NF:winddi.EngUnmapFile
title: EngUnmapFile function
author: windows-driver-content
description: The EngUnmapFile function unmaps the view of a file from system space.
old-location: display\engunmapfile.htm
old-project: display
ms.assetid: e98040c3-4817-470b-9f71-8ebf793fc9a8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EngUnmapFile, EngUnmapFile function [Display Devices], display.engunmapfile, gdifncs_056f6d9c-2c92-4d88-b2b3-f016426d1aed.xml, winddi/EngUnmapFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngUnmapFile
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngUnmapFile function


## -description


The <b>EngUnmapFile</b> function unmaps the view of a file from <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">system space</a>.


## -parameters




### -param iFile [in]

Pointer to the identifier of the mapped file. This identifier was obtained in a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>.


## -returns



<b>EngUnmapFile</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>
 

 

