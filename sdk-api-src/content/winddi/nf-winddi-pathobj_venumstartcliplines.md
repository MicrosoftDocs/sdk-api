---
UID: NF:winddi.PATHOBJ_vEnumStartClipLines
title: PATHOBJ_vEnumStartClipLines function
author: windows-sdk-content
description: The PATHOBJ_vEnumStartClipLines function allows the driver to request lines to be clipped against a specified clip region.
old-location: display\pathobj_venumstartcliplines.htm
old-project: display
ms.assetid: 3db437aa-40d1-4703-ab1e-b3e154923d2d
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: PATHOBJ_vEnumStartClipLines, PATHOBJ_vEnumStartClipLines function [Display Devices], display.pathobj_venumstartcliplines, gdifncs_f5446bec-830c-4946-b899-1d9a957b44ef.xml, winddi/PATHOBJ_vEnumStartClipLines
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
 - PATHOBJ_vEnumStartClipLines
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# PATHOBJ_vEnumStartClipLines function


## -description


The <b>PATHOBJ_vEnumStartClipLines</b> function allows the driver to request lines to be clipped against a specified clip region.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that describes the specified clipping object.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that describes the clip region.


### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that GDI queries to retrieve information about styling steps.


### -param pla

Pointer to a <a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a> structure that GDI queries to retrieve line width and styling information.


## -returns



None




## -remarks



This function is useful when the clip region is more complex than a simple rectangle.

<b>PATHOBJ_vEnumStartClipLines</b> performs calculations for cosmetic wide lines. If the LINEATTRS structure needs a cosmetic wide line, the enumeration walks the given path as many times as needed to complete the widened figure.

This function should not be called for geometric wide lines or paths that contain Bezier curves.

Once begun, this enumeration process should not be restarted.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

