---
UID: NF:wiautil.wiauRegOpenDataW
title: wiauRegOpenDataW function
author: windows-driver-content
description: The wiauRegOpenData function opens the DeviceData registry key.
old-location: image\wiauregopendata.htm
old-project: image
ms.assetid: f289dfa8-26e4-426b-8058-8c2464e47e2a
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiauregopendata, wiauFncs_1718e270-b13c-4325-bb4a-a872becaa8bb.xml, wiauRegOpenData, wiauRegOpenData function [Imaging Devices], wiauRegOpenDataA, wiauRegOpenDataW, wiautil/wiauRegOpenData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiautil.h
api_name:
-	wiauRegOpenData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauRegOpenDataW function


## -description


The <b>wiauRegOpenData</b> function opens the <b>DeviceData</b> registry key.


## -parameters




### -param hkeyAncestor [in]

Specifies the key handle of the parent. This parameter should be set to the value used in the call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method.


### -param phkeyDeviceData [in, out]

Pointer to a memory location that receives the opened key handle.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -remarks



Call this function only in the STI <a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a> method. Call <b>RegCloseKey</b> (described in the Microsoft Windows SDK documentation) when you are finished with the registry.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543824">IStiUSD::Initialize</a>
 

 

