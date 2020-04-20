---
UID: NF:winddi.STROBJ_vEnumStart
title: STROBJ_vEnumStart function (winddi.h)
description: The STROBJ_vEnumStart function defines the form, or type, for data that will be returned from GDI in subsequent calls to STROBJ_bEnum.helpviewer_keywords: ["STROBJ_vEnumStart","STROBJ_vEnumStart function [Display Devices]","display.strobj_venumstart","gdifncs_f0be3fdf-8725-4f9c-8487-0aaa95a13ede.xml","winddi/STROBJ_vEnumStart"]
old-location: display\strobj_venumstart.htm
tech.root: display
ms.assetid: 568af273-2b9d-4782-849f-6cb9c49952e0
ms.date: 12/05/2018
ms.keywords: STROBJ_vEnumStart, STROBJ_vEnumStart function [Display Devices], display.strobj_venumstart, gdifncs_f0be3fdf-8725-4f9c-8487-0aaa95a13ede.xml, winddi/STROBJ_vEnumStart
f1_keywords:
- winddi/STROBJ_vEnumStart
dev_langs:
- c++
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- STROBJ_vEnumStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# STROBJ_vEnumStart function


## -description


The <b>STROBJ_vEnumStart</b> function defines the form, or type, for data that will be returned from GDI in subsequent calls to <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-strobj_benum">STROBJ_bEnum</a>. 


## -parameters




### -param pstro

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a> structure whose data form is to be defined.


## -returns



None




## -remarks



This function also restarts the enumeration of the <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-glyphpos">GLYPHPOS</a> array.

This function should be called by the driver prior to calling <b>STROBJ_bEnum</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-glyphpos">GLYPHPOS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-strobj_benum">STROBJ_bEnum</a>
 

 

