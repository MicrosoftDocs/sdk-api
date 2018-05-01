---
UID: NF:wiautil.wiauStrW2C
title: wiauStrW2C function
author: windows-driver-content
description: The wiauStrW2C function converts a Unicode string to an ANSI character string.
old-location: image\wiaustrw2c.htm
old-project: image
ms.assetid: 53657c26-5007-4c8e-aadf-5d464f1222d2
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaustrw2c, wiauFncs_e97643cb-071d-48bb-82b9-98244bd4284b.xml, wiauStrW2C, wiauStrW2C function [Imaging Devices], wiautil/wiauStrW2C
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
-	wiauStrW2C
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauStrW2C function


## -description


The <b>wiauStrW2C</b> function converts a Unicode string to an ANSI character string.


## -parameters




### -param pwszSrc [in]

Points to the Unicode string to be converted.


### -param pszDst [out]

Pointer to a memory location that receives the converted ANSI string.


### -param iSize

Specifies the size, in bytes, of the buffer pointed to by <i>pszDst</i>.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550183">wiauStrC2C</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550186">wiauStrC2W</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550189">wiauStrW2W</a>
 

 

