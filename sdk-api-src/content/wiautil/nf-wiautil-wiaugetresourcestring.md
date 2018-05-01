---
UID: NF:wiautil.wiauGetResourceString
title: wiauGetResourceString function
author: windows-driver-content
description: The wiauGetResourceString function gets a resource string, storing it as a BSTR.
old-location: image\wiaugetresourcestring.htm
old-project: image
ms.assetid: b042702a-46ff-4ec9-8a92-af8516802e64
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaugetresourcestring, wiauFncs_aa163759-0e49-4612-9f6c-78bd6534a62e.xml, wiauGetResourceString, wiauGetResourceString function [Imaging Devices], wiautil/wiauGetResourceString
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
-	wiauGetResourceString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauGetResourceString function


## -description


The <b>wiauGetResourceString</b> function gets a resource string, storing it as a <b>BSTR</b>.


## -parameters




### -param hInst

Specifies the handle of the module instance.


### -param lResourceID

Specifies the resource ID of the target BSTR value.


### -param pbstrStr [out]

Points to the memory location that receives the retrieved string. The caller of this function must free this string by calling <b>SysFreeString</b> (described in the Microsoft Windows SDK documentation).


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error.



