---
UID: NF:winddi.EngCreateClip
title: EngCreateClip function
author: windows-sdk-content
description: The EngCreateClip function creates a CLIPOBJ structure that the driver uses in callbacks.
old-location: display\engcreateclip.htm
tech.root: display
ms.assetid: 719b006f-1eb0-41c6-8b88-c8241a394abe
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EngCreateClip, EngCreateClip function [Display Devices], display.engcreateclip, gdifncs_e1faed88-1f89-49c2-871e-097e56db1a10.xml, winddi/EngCreateClip
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
 - EngCreateClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngCreateClip function


## -description


The <b>EngCreateClip</b> function creates a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that the driver uses in callbacks. 


## -parameters






## -returns



The return value is a pointer to the newly-created CLIPOBJ structure if the function succeeds. Otherwise, it is <b>NULL</b>.




## -remarks



The CLIPOBJ structure created by <b>EngCreateClip</b> allows GDI to directly access banked frame buffers. The structure must be initialized by the driver so that the <b>iDComplexity</b> member of the CLIPOBJ structure is set to DC_TRIVIAL or DC_RECT. If the <b>iDComplexity</b> member is set to DC_RECT, the driver can set the <b>rclBounds</b> member of CLIPOBJ to the extent of the frame buffer bank. The driver must delete this CLIPOBJ structure using <a href="https://msdn.microsoft.com/7af85df1-1e37-4a69-82a0-1c1eec32dd48">EngDeleteClip</a>.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/7af85df1-1e37-4a69-82a0-1c1eec32dd48">EngDeleteClip</a>
 

 

