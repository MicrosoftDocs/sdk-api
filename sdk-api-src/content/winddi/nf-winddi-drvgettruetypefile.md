---
UID: NF:winddi.DrvGetTrueTypeFile
title: DrvGetTrueTypeFile function
author: windows-sdk-content
description: The DrvGetTrueTypeFile function accesses a memory-mapped TrueType font file.
old-location: display\drvgettruetypefile.htm
old-project: display
ms.assetid: a9e83067-1fd2-4f31-ac6e-545623613f88
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvGetTrueTypeFile, DrvGetTrueTypeFile function [Display Devices], ddifncs_ce14ab7e-837a-4e44-bae6-7630912ff16a.xml, display.drvgettruetypefile, winddi/DrvGetTrueTypeFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvGetTrueTypeFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvGetTrueTypeFile function


## -description


The <b>DrvGetTrueTypeFile</b> function accesses a memory-mapped TrueType font file.


## -parameters




### -param iFile

Pointer to a driver-defined value that identifies a driver's TrueType font file.


### -param pcj

Pointer to a ULONG value that specifies the size, in bytes, of the font file. This parameter cannot be <b>NULL</b>.


## -returns



The return value is a pointer to the memory-mapped TrueType font file if the function is successful. Otherwise, it is <b>NULL</b>.




## -remarks



This private entry point is provided by the TrueType driver to allow GDI efficient access to the memory-mapped TrueType font file.

<b>DrvGetTrueTypeFile</b> is required for TrueType font drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>
 

 

