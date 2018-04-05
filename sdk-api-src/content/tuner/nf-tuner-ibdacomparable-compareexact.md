---
UID: NF:tuner.IBDAComparable.CompareExact
title: IBDAComparable::CompareExact method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibdacomparable_compareexact.htm
old-project: mstv
ms.assetid: 65053d86-4c8c-4c68-90a6-118454cf2eb1
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CompareExact method [Microsoft TV Technologies], CompareExact method [Microsoft TV Technologies], IBDAComparable interface, CompareExact,IBDAComparable.CompareExact, IBDAComparable, IBDAComparable interface [Microsoft TV Technologies], CompareExact method, IBDAComparable::CompareExact, IBDAComparableCompareExact, mstv.ibdacomparable_compareexact, tuner/IBDAComparable::CompareExact
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IBDAComparable.CompareExact
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IBDAComparable::CompareExact method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>CompareExact</b> method compares two objects to determine whether they contain the same tuning information.


## -parameters




### -param CompareTo [in]

Pointer to the <b>IDispatch</b> interface of the object that is to be compared with the object that implements the <b>IBDAComparable</b> interface.


### -param Result [out]

Pointer to a variable that receives the result of the comparison. If the result is 0, the two objects are the same. If the result is nonzero, the two objects are not the same.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method compares two objects to determine whether they contain the same tuning properties. The first object in the comparison is the object that implements the <b>IBDAComparable</b> interface that the method is called on. The <i>CompareTo</i> parameter specifies the second object.

This method compares all of the tuning properties of the two objects and their associated objects. In contrast, the <a href="https://msdn.microsoft.com/132c326e-053c-41be-b0fd-bea484fb0acd">CompareEquivalent</a> method compares only a subset of these properties.

For example, DirectShow implements the <b>IBDAComparable::CompareExact</b> method for a tune-request object to include both the tuning space and locator in the comparison. Thus, two DVB tuning requests are the same only if they both tune to the same DVB URL (with the same original network ID, transport stream ID, and service ID) <i>and</i> have the same modulation type.




## -see-also




<a href="https://msdn.microsoft.com/6f582ae2-d8c6-4d85-a01f-e98c6ee16021">IBDAComparable Interface</a>
 

 

