---
UID: NF:tuner.IBDAComparable.HashEquivalent
title: IBDAComparable::HashEquivalent
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibdacomparable_hashequivalent.htm
old-project: mstv
ms.assetid: 31f52445-a4f5-40f5-ad55-30f3b43b1528
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: HashEquivalent, HashEquivalent method [Microsoft TV Technologies], HashEquivalent method [Microsoft TV Technologies],IBDAComparable interface, IBDAComparable interface [Microsoft TV Technologies],HashEquivalent method, IBDAComparable.HashEquivalent, IBDAComparable::HashEquivalent, IBDAComparableHashEquivalent, mstv.ibdacomparable_hashequivalent, tuner/IBDAComparable::HashEquivalent
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
-	IBDAComparable.HashEquivalent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IBDAComparable::HashEquivalent


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>HashEquivalent</b> method generates a hash code for a subset of the tuning properties of an object.


## -parameters




### -param dwFlags [in]

Specifies whether to alter the subset of properties that are to be incorporated by default into the hash code. Setting this parameter to 0 invokes the default behavior. Setting this parameter to the bitwise <b>OR</b> of one or more <a href="https://msdn.microsoft.com/3bf4b82d-29d2-442e-ad20-bdb7ef66dfb5">BDA_Comp_Flags</a> enumeration values overrides the default behavior.


### -param Result [out]

Pointer to a variable that receives the result of the hash operation. This result is the hash code for the subset of the tuning properties of the object and its associated objects that are to be included in comparisons with other objects.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method generates a hash code from a subset of the tuning properties in the object that implements the <a href="https://msdn.microsoft.com/6f582ae2-d8c6-4d85-a01f-e98c6ee16021">IBDAComparable</a> interface, and its associated objects.

The caller can compare the resulting hash code to the hash code for another object of the same type to determine whether the two objects contain equivalent tuning information. The hash code incorporates only the subset of properties in the object and its associated objects that is required to determine whether the properties are equivalent to those in another object. If the hash codes for the two objects are identical, the two objects contain equivalent tuning information.




## -see-also




<a href="https://msdn.microsoft.com/8e5fcaf0-f160-4cff-9e9d-44766e0545c9">HashEquivalentIncremental</a>



<a href="https://msdn.microsoft.com/6f582ae2-d8c6-4d85-a01f-e98c6ee16021">IBDAComparable Interface</a>
 

 

