---
UID: NF:wiautil.wiauStrW2W
title: wiauStrW2W function
author: windows-driver-content
description: The wiauStrW2W function copies a Unicode string to another Unicode string.
old-location: image\wiaustrw2w.htm
old-project: image
ms.assetid: 84f6d47f-bd14-4df4-b4fa-e58412daba6f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaustrw2w, wiauFncs_4778241e-19d0-40e1-ae24-e58e950ba540.xml, wiauStrW2W, wiauStrW2W function [Imaging Devices], wiautil/wiauStrW2W
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
-	wiauStrW2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauStrW2W function


## -description


The <b>wiauStrW2W</b> function copies a Unicode string to another Unicode string.


## -parameters




### -param pwszSrc [in]

Points to the Unicode string to be copied.


### -param pwszDst [out]

Pointer to a memory location that receives the copied string.


### -param iSize

Specifies the size, in bytes, of the buffer pointed to by <i>pwszDst</i>.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550183">wiauStrC2C</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550186">wiauStrC2W</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550187">wiauStrW2C</a>
 

 

