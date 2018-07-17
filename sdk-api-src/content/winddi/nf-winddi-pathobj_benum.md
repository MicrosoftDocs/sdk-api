---
UID: NF:winddi.PATHOBJ_bEnum
title: PATHOBJ_bEnum function
author: windows-sdk-content
description: The PATHOBJ_bEnum function retrieves the next PATHDATA record from a specified path and enumerates the curves in the path.
old-location: display\pathobj_benum.htm
old-project: display
ms.assetid: 2e8bd76c-5ee6-4fe5-b1e5-64e84d09fc8f
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: PATHOBJ_bEnum, PATHOBJ_bEnum function [Display Devices], display.pathobj_benum, gdifncs_afa2e11c-1671-426c-aab8-c0998eafb4b5.xml, winddi/PATHOBJ_bEnum
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
 - PATHOBJ_bEnum
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# PATHOBJ_bEnum function


## -description


The <b>PATHOBJ_bEnum</b> function retrieves the next PATHDATA record from a specified path and enumerates the curves in the path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure whose curves and/or lines are to be enumerated.


### -param ppd

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PATHDATA</a> structure that is to be filled.


## -returns



The return value is <b>TRUE</b> if the specified path contains more PATHDATA records, indicating that this service should be called again. Otherwise, if the output is the last PATHDATA record in the path, the return value is <b>FALSE</b>.




## -remarks



<b>PATHOBJ_bEnum</b> can be called only after a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568856">PATHOBJ_vEnumStart</a> has been made.

A PATHDATA structure describes all or part of a subpath (a connected part of a path). For example, a <b>MoveTo</b> call by the application within a path begins a new subpath.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PATHDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568856">PATHOBJ_vEnumStart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>
 

 

