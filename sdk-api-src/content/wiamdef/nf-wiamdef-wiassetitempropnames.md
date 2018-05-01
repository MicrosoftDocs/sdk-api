---
UID: NF:wiamdef.wiasSetItemPropNames
title: wiasSetItemPropNames function
author: windows-driver-content
description: The wiasSetItemPropNames function writes property names to item properties.
old-location: image\wiassetitempropnames.htm
old-project: image
ms.assetid: 4140a6c6-60e8-41ec-8de0-cfb56e757e34
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiassetitempropnames, wiamdef/wiasSetItemPropNames, wiasFncs_e8f17c14-47a7-42bc-ad85-cdd52ecbab79.xml, wiasSetItemPropNames, wiasSetItemPropNames function [Imaging Devices]
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
-	wiasSetItemPropNames
product: Windows
targetos: Windows
req.lib: Wiaservc.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# wiasSetItemPropNames function


## -description


The <b>wiasSetItemPropNames </b>function writes property names to item properties.


## -parameters




### -param pWiasContext [in]

Pointer to a WIA item context.


### -param cItemProps

Specifies the number of property names to write.


### -param ppId [in, out]

Pointer to the first element of a caller-allocated array of property identifiers (PROPIDs).


### -param ppszNames

TBD




#### - ppSzNames [in, out]

Pointer to the first element of a caller-allocated array of property names to write.


## -returns



On success, the function returns S_OK. If the function fails, it returns a standard COM error or one of the WIA_ERROR_XXX errors (described in the Microsoft Windows SDK documentation).




## -remarks



Minidrivers typically use this function when initializing item properties. The order of property identifiers in <i>ppId</i> must match the order of property names in <i>ppSzNames</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549358">wiasSetItemPropAttribs</a>
 

 

