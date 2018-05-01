---
UID: NF:wiamdef.wiasCreateChildAppItem
title: wiasCreateChildAppItem function
author: windows-driver-content
description: The wiasCreateChildAppItem function creates a new application item and inserts it as a child of the specified (parent) item. Note that this item will not have any properties in its property sets until the driver or application actually fills them in.
old-location: image\wiascreatechildappitem.htm
old-project: image
ms.assetid: 1dba59b0-5eac-4507-bd42-517a856aa864
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiascreatechildappitem, wiamdef/wiasCreateChildAppItem, wiasCreateChildAppItem, wiasCreateChildAppItem function [Imaging Devices], wiasFncs_63e9cbb1-6435-433b-a27f-36b66042be8a.xml
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
-	wiasCreateChildAppItem
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasCreateChildAppItem function


## -description


The <b>wiasCreateChildAppItem</b> function creates a new application item and inserts it as a child of the specified (parent) item. Note that this item will not have any properties in its property sets until the driver or application actually fills them in.


## -parameters




### -param pParentWiasContext [in]

Pointer to the item context to which the child will be added.


### -param lFlags

Is reserved for system use.  


### -param bstrItemName [in]

Specifies a string that contains the item name without path information.


### -param bstrFullItemName [in]

Specifies a string that contains the item name including path information.


### -param ppWiasChildContext [out]

Pointer to a memory location that receives the address of the newly created child item's context.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549160">wiasCreateDrvItem</a>
 

 

