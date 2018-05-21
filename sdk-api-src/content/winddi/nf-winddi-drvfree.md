---
UID: NF:winddi.DrvFree
title: DrvFree function
author: windows-driver-content
description: The DrvFree function is used to notify the driver that the specified structure is no longer needed.
old-location: display\drvfree.htm
old-project: display
ms.assetid: 829e8128-f57f-433c-9c09-7e4dc0ef54be
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: DrvFree, DrvFree function [Display Devices], ddifncs_c3b37742-3ce6-477b-a28c-065cd60c38cd.xml, display.drvfree, winddi/DrvFree
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvFree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvFree function


## -description


The <b>DrvFree</b> function is used to notify the driver that the specified structure is no longer needed.


## -parameters




### -param pv

Pointer to the structure whose memory is to be freed.


### -param id

Pointer to the identifier that was returned with the structure.


## -returns



None




## -remarks



<b>DrvFree</b> is an optional function that should be supported only if the driver must be informed when memory associated with structures can be freed. For example, if a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure is in use, deletion can be deferred until <a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a> has been called, eliminating the need for the driver to implement <b>DrvFree</b>.

A driver can use <i>id</i> in different ways. It can specify an object handle or it can indicate the way the structure is allocated. For example, it can differentiate between loaded resources and memory allocated from a heap. The driver can ignore this parameter if the structure pointed to by <i>pv</i> contains enough information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556262">DrvQueryFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>
 

 

