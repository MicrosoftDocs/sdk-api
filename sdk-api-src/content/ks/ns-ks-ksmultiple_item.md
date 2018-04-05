---
UID: NS:ks.KSMULTIPLE_ITEM
title: KSMULTIPLE_ITEM
author: windows-driver-content
description: The KSMULTIPLE_ITEM structure describes the size and count of variable-length properties on kernel-mode pins.
old-location: dshow\ksmultiple_item.htm
old-project: DirectShow
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PKSMULTIPLE_ITEM, KSMULTIPLE_ITEM, KSMULTIPLE_ITEM structure [DirectShow], KSMULTIPLE_ITEMStructure, PKSMULTIPLE_ITEM, PKSMULTIPLE_ITEM structure pointer [DirectShow], dshow.ksmultiple_item, ks/KSMULTIPLE_ITEM, ks/PKSMULTIPLE_ITEM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ks.h
req.include-header: 
req.target-type: Windows
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
req.typenames: KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ks.h
api_name:
-	KSMULTIPLE_ITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# KSMULTIPLE_ITEM structure


## -description



The <code>KSMULTIPLE_ITEM</code> structure describes the size and count of variable-length properties on kernel-mode pins.




## -struct-fields




### -field Size

Size of the returned memory block, in bytes. The size includes the <b>KSMULTIPLE_ITEM</b> structure and the items that follow it.


### -field Count

Specifies the total number of items that follow this structure.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560717">IKsPin::KsQueryMediums</a>



<a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a>
 

 

