---
UID: NF:winddi.PATHOBJ_vEnumStart
title: PATHOBJ_vEnumStart function (winddi.h)
description: The PATHOBJ_vEnumStart function notifies a given PATHOBJ structure that the driver will be calling PATHOBJ_bEnum to enumerate lines and/or curves in the path.
helpviewer_keywords: ["PATHOBJ_vEnumStart","PATHOBJ_vEnumStart function [Display Devices]","display.pathobj_venumstart","gdifncs_93ed4330-ebfd-4ba1-b095-99beb3146452.xml","winddi/PATHOBJ_vEnumStart"]
old-location: display\pathobj_venumstart.htm
tech.root: display
ms.assetid: b83e6f87-be79-4743-bc52-b9310853c4f5
ms.date: 12/05/2018
ms.keywords: PATHOBJ_vEnumStart, PATHOBJ_vEnumStart function [Display Devices], display.pathobj_venumstart, gdifncs_93ed4330-ebfd-4ba1-b095-99beb3146452.xml, winddi/PATHOBJ_vEnumStart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PATHOBJ_vEnumStart
 - winddi/PATHOBJ_vEnumStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - PATHOBJ_vEnumStart
---

# PATHOBJ_vEnumStart function


## -description

The <b>PATHOBJ_vEnumStart</b> function notifies a given PATHOBJ structure that the driver will be calling <a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benum">PATHOBJ_bEnum</a> to enumerate lines and/or curves in the path.

## -parameters

### -param ppo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure whose lines and/or curves are to be enumerated.

## -returns

None

## -remarks

<b>PATHOBJ_vEnumStart</b> can be called at any time to restart an enumeration.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-pathobj_benum">PATHOBJ_bEnum</a>