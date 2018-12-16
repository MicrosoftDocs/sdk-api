---
UID: NF:tuner.IBDAComparable.HashExact
title: IBDAComparable::HashExact
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\ibdacomparable_hashexact.htm
tech.root: mstv
ms.assetid: 41495662-835b-47bc-a8d6-b0b689ec4d51
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HashExact, HashExact method [Microsoft TV Technologies], HashExact method [Microsoft TV Technologies],IBDAComparable interface, IBDAComparable interface [Microsoft TV Technologies],HashExact method, IBDAComparable.HashExact, IBDAComparable::HashExact, IBDAComparableHashExact, mstv.ibdacomparable_hashexact, tuner/IBDAComparable::HashExact
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IBDAComparable.HashExact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDAComparable::HashExact


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>HashExact</b> method generates a hash code for all of the tuning properties of an object.


## -parameters




### -param Result [out]

Receives the result of the hash operation. This result is the hash code for the tuning properties of the object and its associated objects that are to be included in comparisons with other objects.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method generates a hash code from the values of the tuning properties in the object that implements the <b>IBDAComparable</b> interface, and its associated objects.

The caller can compare the resulting hash code to the hash code for another object of the same type to determine whether the two objects contain the same tuning information. The hash code incorporates the tuning properties in the object and its associated objects. If the hash codes for the two objects are identical, the two objects contain the same tuning information.




## -see-also




<a href="https://msdn.microsoft.com/4ddf2545-83a6-4b5d-94ba-7034aed61f08">HashExactIncremental</a>



<a href="https://msdn.microsoft.com/6f582ae2-d8c6-4d85-a01f-e98c6ee16021">IBDAComparable Interface</a>
 

 

