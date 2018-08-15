---
UID: NF:winddi.EngCreatePath
title: EngCreatePath function
author: windows-sdk-content
description: The EngCreatePath function allocates a path for the driver's temporary use.
old-location: display\engcreatepath.htm
old-project: display
ms.assetid: b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngCreatePath, EngCreatePath function [Display Devices], display.engcreatepath, gdifncs_73e7c8ea-ed9f-4479-bd8a-86a5d07e5d33.xml, winddi/EngCreatePath
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
 - EngCreatePath
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCreatePath function


## -description


The <b>EngCreatePath</b> function allocates a path for the driver's temporary use. 


## -parameters






## -returns



The return value is a pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure if the function is successful. Otherwise, it is null, and an error code is logged.




## -remarks



The driver should delete the path, allocated by <b>EngCreatePath</b>, before returning to GDI from its current drawing call.

Functions that create and modify paths are provided to assist devices in clipping paths. A driver can create a path, fill it with lines and pass the path to <a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a> for clipping against the complex region.

A PATHOBJ structure is a locked object, and thus should not be locked for a long time by the driver.

If the driver uses <b>EngCreatePath</b> to create a PATHOBJ structure, it should be deleted by using <a href="https://msdn.microsoft.com/65ecf4bc-5180-4b4b-a359-298f385b849e">EngDeletePath</a> as soon as the driver finishes with it.

The returned PATHOBJ structure is used in calls to <a href="https://msdn.microsoft.com/b734ce8f-7e7e-4c13-a614-cb6b0dc19ead">PATHOBJ_bMoveTo</a>, <a href="https://msdn.microsoft.com/468d20e3-a78b-47b3-9c56-ef355181eb63">PATHOBJ_bPolyLineTo</a>, <a href="https://msdn.microsoft.com/3db437aa-40d1-4703-ab1e-b3e154923d2d">PATHOBJ_vEnumStartClipLines</a>, and <a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>





## -see-also




<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>
 

 

