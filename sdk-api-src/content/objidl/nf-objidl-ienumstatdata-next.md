---
UID: NF:objidl.IEnumSTATDATA.Next
title: IEnumSTATDATA::Next (objidl.h)
author: windows-sdk-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: com\ienumstatdata_next.htm
tech.root: com
ms.assetid: 8258b6f4-15d7-4da2-96d1-d1ce36a31c1c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSTATDATA interface [COM],Next method, IEnumSTATDATA.Next, IEnumSTATDATA::Next, Next, Next method [COM], Next method [COM],IEnumSTATDATA interface, _ole_ienumstatdata_next, com.ienumstatdata_next, objidl/IEnumSTATDATA::Next
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IEnumSTATDATA.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATDATA::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.


### -param rgelt [out]

An array of enumerated items.

The enumerator is responsible for allocating any memory, and the caller is responsible for freeing it. If <i>celt</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pceltFetched</i> to know how many pointers to release.


### -param pceltFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b> if <i>celt</i> is 1.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>



<a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a>
 

 

