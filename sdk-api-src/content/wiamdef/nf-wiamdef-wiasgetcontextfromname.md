---
UID: NF:wiamdef.wiasGetContextFromName
title: wiasGetContextFromName function
author: windows-driver-content
description: The wiasGetContextFromName function retrieves the item context for an item name.
old-location: image\wiasgetcontextfromname.htm
old-project: image
ms.assetid: d15bf48e-132d-4f89-8f19-64f57deed500
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiasgetcontextfromname, wiamdef/wiasGetContextFromName, wiasFncs_ba1c88a2-aadc-4c2f-bb5f-88433d1e1760.xml, wiasGetContextFromName, wiasGetContextFromName function [Imaging Devices]
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
-	wiasGetContextFromName
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasGetContextFromName function


## -description


The <b>wiasGetContextFromName</b> function retrieves the item context for an item name.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param lFlags

Reserved for system use and should be set to 0.


### -param bstrName [in]

Specifies the name of the context that is being searched for.


### -param ppWiasContext [out]

Pointer to a memory location that receives the address of the WIA item context.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



This function searches for item contexts whose WIA_IPA_FULL_ITEM_NAME property matches <i>bstrName</i>. Note that this property is different from WIA_IPA_ITEM_NAME, which does not contain path information.

This function should be used by minidrivers when they need to move from one application item context to another, given the item's name. The names of the application items come from their corresponding driver items, which the minidriver creates and names. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549264">wiasGetRootItem</a>
 

 

