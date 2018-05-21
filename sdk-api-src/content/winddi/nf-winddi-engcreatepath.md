---
UID: NF:winddi.EngCreatePath
title: EngCreatePath function
author: windows-driver-content
description: The EngCreatePath function allocates a path for the driver's temporary use.
old-location: display\engcreatepath.htm
old-project: display
ms.assetid: b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: EngCreatePath, EngCreatePath function [Display Devices], display.engcreatepath, gdifncs_73e7c8ea-ed9f-4479-bd8a-86a5d07e5d33.xml, winddi/EngCreatePath
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
-	EngCreatePath
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



The return value is a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure if the function is successful. Otherwise, it is null, and an error code is logged.




## -remarks



The driver should delete the path, allocated by <b>EngCreatePath</b>, before returning to GDI from its current drawing call.

Functions that create and modify paths are provided to assist devices in clipping paths. A driver can create a path, fill it with lines and pass the path to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a> for clipping against the complex region.

A PATHOBJ structure is a locked object, and thus should not be locked for a long time by the driver.

If the driver uses <b>EngCreatePath</b> to create a PATHOBJ structure, it should be deleted by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564811">EngDeletePath</a> as soon as the driver finishes with it.

The returned PATHOBJ structure is used in calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568853">PATHOBJ_bMoveTo</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff568855">PATHOBJ_bPolyLineTo</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568852">PATHOBJ_bEnumClipLines</a>
 

 

