---
UID: NF:winddi.DrvDestroyFont
title: DrvDestroyFont function
author: windows-sdk-content
description: The DrvDestroyFont function notifies the driver that a font realization is no longer needed and that the driver can now free any associated data structures it has allocated.
old-location: display\drvdestroyfont.htm
old-project: display
ms.assetid: aee3efbc-715d-42f2-a718-00057720175a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvDestroyFont, DrvDestroyFont function [Display Devices], ddifncs_a73e0b14-897a-423d-a9db-8c4ba831a36b.xml, display.drvdestroyfont, winddi/DrvDestroyFont
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDestroyFont
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvDestroyFont function


## -description


The <b>DrvDestroyFont</b> function notifies the driver that a font realization is no longer needed and that the driver can now free any associated data structures it has allocated.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure that identifies the font instance.


## -returns



None




## -remarks



The <b>DrvDestroyFont</b> function is called only in font drivers and kernel-mode printer drivers. 

If the DEVICE_FONTTYPE flag is set in the <b>flFontType</b> member of the FONTOBJ structure, the driver should release any resources or memory identified with both the <b>pvConsumer</b> and <b>pvProducer</b> members of FONTOBJ. Otherwise, it should release only memory and resources identified with <b>pvConsumer</b>.

The driver must reset the <b>pvConsumer</b> and <b>pvProducer</b> members to <b>NULL</b> if it uses them.

GDI calls <b>DrvDestroyFont</b> once for the font producer and once again for the font consumer.

GDI guarantees that <b>DrvDestroyFont</b> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> never overlap; consequently, the driver can rely on cached information while processing a <b>DrvTextOut</b> call.

This function must be implemented if the font driver or kernel-mode printer driver allocates resources when it realizes fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

