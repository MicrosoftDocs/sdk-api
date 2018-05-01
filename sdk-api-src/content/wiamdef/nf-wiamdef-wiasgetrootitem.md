---
UID: NF:wiamdef.wiasGetRootItem
title: wiasGetRootItem function
author: windows-driver-content
description: The wiasGetRootItem function retrieves the root item context of a specified WIA item.
old-location: image\wiasgetrootitem.htm
old-project: image
ms.assetid: 09885782-2293-49a3-af48-6450dbc6a24e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetrootitem, wiamdef/wiasGetRootItem, wiasFncs_4e991723-5462-456e-b56f-82a38e5cf556.xml, wiasGetRootItem, wiasGetRootItem function [Imaging Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wiaservc.dll
api_name:
-	wiasGetRootItem
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetRootItem function


## -description


The <b>wiasGetRootItem</b> function retrieves the root item context of a specified WIA item.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param ppWiasContext [out]

Pointer to a memory location that receives the address of the WIA item's root item context.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549243">wiasGetDrvItem</a>
 

 

