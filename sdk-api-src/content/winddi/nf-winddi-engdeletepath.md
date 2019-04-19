---
UID: NF:winddi.EngDeletePath
title: EngDeletePath function (winddi.h)
author: windows-sdk-content
description: The EngDeletePath function deletes a path previously allocated by EngCreatePath.
old-location: display\engdeletepath.htm
tech.root: display
ms.assetid: 65ecf4bc-5180-4b4b-a359-298f385b849e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngDeletePath, EngDeletePath function [Display Devices], display.engdeletepath, gdifncs_aa1e2ccc-cc76-4782-b2ff-9867576c82d1.xml, winddi/EngDeletePath
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
 - EngDeletePath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngDeletePath function


## -description


The <b>EngDeletePath</b> function deletes a path previously allocated by <a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>.


## -parameters




### -param ppo

Pointer to the <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure to be deleted.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>
 

 

