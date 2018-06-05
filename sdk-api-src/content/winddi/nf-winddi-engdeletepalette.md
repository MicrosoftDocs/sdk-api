---
UID: NF:winddi.EngDeletePalette
title: EngDeletePalette function
author: windows-sdk-content
description: The EngDeletePalette function sends a request to GDI to delete the specified palette.
old-location: display\engdeletepalette.htm
old-project: display
ms.assetid: ebdbbb4e-aaa8-4fb7-9546-545dce803054
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngDeletePalette, EngDeletePalette function [Display Devices], display.engdeletepalette, gdifncs_221095fd-b5c5-485e-9e8c-9f7a114d496d.xml, winddi/EngDeletePalette
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngDeletePalette
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeletePalette function


## -description


The <b>EngDeletePalette</b> function sends a request to GDI to delete the specified palette.


## -parameters




### -param hpal [in]

Handle to the palette to be deleted. This handle is supplied by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564212">EngCreatePalette</a>.


## -returns



The return value is <b>TRUE</b> if the function is successful; otherwise, it returns <b>FALSE</b>.



