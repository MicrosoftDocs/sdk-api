---
UID: NF:winddi.EngCreateDeviceSurface
title: EngCreateDeviceSurface function
author: windows-sdk-content
description: The EngCreateDeviceSurface function creates and returns a handle for a device surface that the driver will manage.
old-location: display\engcreatedevicesurface.htm
old-project: display
ms.assetid: 9c3ca4c4-7614-4739-8333-202c6ec2eab8
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngCreateDeviceSurface, EngCreateDeviceSurface function [Display Devices], display.engcreatedevicesurface, gdifncs_0a48d849-3e93-4310-87e1-cd0b6882b4a4.xml, winddi/EngCreateDeviceSurface
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
 - EngCreateDeviceSurface
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCreateDeviceSurface function


## -description


The <b>EngCreateDeviceSurface</b> function creates and returns a handle for a device surface that the driver will manage.


## -parameters




### -param dhsurf [in]

Device handle to the surface to be managed by the device. This handle is passed to the driver when a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure is passed for input or output.


### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the surface to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the surface's width and height, in pixels. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call.


## -returns



The return value is a handle that identifies the surface if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



The storage space for the surface can optionally be provided by the driver. The surface should be associated by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>. The surface should be deleted when it is no longer needed by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

