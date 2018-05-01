---
UID: NF:winddi.WNDOBJ_vSetConsumer
title: WNDOBJ_vSetConsumer function
author: windows-driver-content
description: The WNDOBJ_vSetConsumer function sets a driver-defined value in the pvConsumer field of the specified WNDOBJ structure.
old-location: display\wndobj_vsetconsumer.htm
old-project: display
ms.assetid: c7b550b8-1a3f-4d69-93d1-241044cb4bbd
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: WNDOBJ_vSetConsumer, WNDOBJ_vSetConsumer function [Display Devices], display.wndobj_vsetconsumer, gdifncs_759188da-41cc-45c8-845f-80d23e60e88b.xml, winddi/WNDOBJ_vSetConsumer
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
-	WNDOBJ_vSetConsumer
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# WNDOBJ_vSetConsumer function


## -description


The <b>WNDOBJ_vSetConsumer</b> function sets a driver-defined value in the <b>pvConsumer</b> field of the specified <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure created by a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>.


### -param pvConsumer

A driver-defined value for identifying this particular WNDOBJ structure. This value overrides the previous value stored in the WNDOBJ structure.


## -returns



None




## -remarks



<b>WNDOBJ_vSetConsumer</b> should be called only by the following functions:

<ul>
<li>
Graphics DDI functions for which a WNDOBJ structure is provided.

</li>
<li>
The callback provided to GDI by a driver's call to <b>EngCreateWnd</b>.

</li>
<li>
The WNDOBJ_SETUP escape defined by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a> after a new WNDOBJ structure is created.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556217">DrvEscape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>
 

 

