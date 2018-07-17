---
UID: NF:winddi.FONTOBJ_pjOpenTypeTablePointer
title: FONTOBJ_pjOpenTypeTablePointer function
author: windows-sdk-content
description: The FONTOBJ_pjOpenTypeTablePointer function returns a pointer to a view of an OpenType table.
old-location: display\fontobj_pjopentypetablepointer.htm
old-project: display
ms.assetid: d41728f7-f5b5-40cd-b690-cb1f8161f6c1
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: FONTOBJ_pjOpenTypeTablePointer, FONTOBJ_pjOpenTypeTablePointer function [Display Devices], display.fontobj_pjopentypetablepointer, gdifncs_c8a7074e-3a62-426b-a1d2-57b04441f7f8.xml, winddi/FONTOBJ_pjOpenTypeTablePointer
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FONTOBJ_pjOpenTypeTablePointer
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# FONTOBJ_pjOpenTypeTablePointer function


## -description


The <b>FONTOBJ_pjOpenTypeTablePointer</b> function returns a pointer to a view of an OpenType table.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> that identifies the font whose OpenType table is being queried.


### -param ulTag

Identifies the font table whose pointer is to be returned.


### -param pcjTable

Pointer to the location in which GDI returns the size in bytes of the table being queried.


## -returns



<b>FONTOBJ_pjOpenTypeTablePointer</b> returns a pointer to a view of the OpenType table. A return value of <b>NULL</b> indicates that the requested table is not present in this font.




## -remarks



<b>FONTOBJ_pjOpenTypeTablePointer</b> can be called by printer drivers that can download OpenType fonts or parts of OpenType fonts to the printer.

The pointer to a table returned by <b>FONTOBJ_pjOpenTypeTablePointer</b> is guaranteed to be valid only during the scope of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> call to which <i>pfo</i> is passed as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

