---
UID: NF:winddi.XLATEOBJ_iXlate
title: XLATEOBJ_iXlate function
author: windows-sdk-content
description: The XLATEOBJ_iXlate function translates a color index of the source palette to the closest index in the destination palette.
old-location: display\xlateobj_ixlate.htm
old-project: display
ms.assetid: 1506efcb-d4fa-4120-89ba-5aca0f3c7f97
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: XLATEOBJ_iXlate, XLATEOBJ_iXlate function [Display Devices], display.xlateobj_ixlate, gdifncs_c1ca950a-fb95-47ae-936a-857ffc47c027.xml, winddi/XLATEOBJ_iXlate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - XLATEOBJ_iXlate
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# XLATEOBJ_iXlate function


## -description


The <b>XLATEOBJ_iXlate</b> function translates a color index of the source palette to the closest index in the destination palette.


## -parameters




### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that defines the source palette.


### -param iColor

Specifies the color index to be translated.


## -returns



The return value is an index into the destination palette if the function is successful. If the function fails, -1 is returned.




## -see-also




<a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a>
 

 

