---
UID: NF:winddi.DrvDisablePDEV
title: DrvDisablePDEV function
author: windows-driver-content
description: The DrvDisablePDEV function is used by GDI to notify a driver that the specified PDEV is no longer needed.
old-location: display\drvdisablepdev.htm
old-project: display
ms.assetid: dff04000-e307-4a1c-80fe-d6666929df76
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: DrvDisablePDEV, DrvDisablePDEV function [Display Devices], ddifncs_ff781393-2fad-482c-a91e-1cf0b722441d.xml, display.drvdisablepdev, winddi/DrvDisablePDEV
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvDisablePDEV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvDisablePDEV function


## -description


The <b>DrvDisablePDEV</b> function is used by GDI to notify a driver that the specified <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> is no longer needed.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> of the physical device to be disabled. This value is the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


## -returns



None




## -remarks



If the physical device has an enabled surface, GDI calls <b>DrvDisablePDEV</b> after calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff556200">DrvDisableSurface</a>. The driver should free any memory and resources used by the PDEV.

<b>DrvDisablePDEV</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556200">DrvDisableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>
 

 

