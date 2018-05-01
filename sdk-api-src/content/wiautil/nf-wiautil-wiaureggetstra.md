---
UID: NF:wiautil.wiauRegGetStrA
title: wiauRegGetStrA function
author: windows-driver-content
description: The wiauRegGetStr function gets a string value from the DeviceData section of the registry.
old-location: image\wiaureggetstr.htm
old-project: image
ms.assetid: ff06737b-c37d-4f37-adfc-bbd51974c9e4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaureggetstr, wiauFncs_b9145502-734d-40de-8086-c1f193966269.xml, wiauRegGetStr, wiauRegGetStr function [Imaging Devices], wiauRegGetStrA, wiauRegGetStrW, wiautil/wiauRegGetStr
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
-	wiauRegGetStr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauRegGetStrA function


## -description


The <b>wiauRegGetStr</b> function gets a string value from the <b>DeviceData</b> section of the registry.


## -parameters




### -param hkKey [in]

Specifies the registry key handle. This parameter should be set to the value pointed to by the <i>phkeyDeviceData </i>parameter when <a href="https://msdn.microsoft.com/library/windows/hardware/ff550179">wiauRegOpenData</a> returns.


### -param pszValueName

TBD


### -param pszValue

TBD


### -param pdwLength [in, out]

Pointer to a memory location that receives the length, in bytes, of the string value pointed to by the <i>pwszValue</i> parameter. The length includes the terminating null character.


#### - pwszValue [out]

Pointer to a memory location that receives the string value, including a terminating null character.


#### - pwszValueName [in]

Points to the first character of a Unicode string containing the name of the registry entry.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550176">wiauRegGetDword</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550179">wiauRegOpenData</a>
 

 

