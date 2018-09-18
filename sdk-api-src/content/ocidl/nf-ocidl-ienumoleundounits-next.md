---
UID: NF:ocidl.IEnumOleUndoUnits.Next
title: IEnumOleUndoUnits::Next
author: windows-sdk-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: com\ienumoleundounits_next.htm
tech.root: com
ms.assetid: bd5ce157-37d1-4e27-a0d4-ed9cffeac2b3
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IEnumOleUndoUnits interface [COM],Next method, IEnumOleUndoUnits.Next, IEnumOleUndoUnits::Next, Next, Next method [COM], Next method [COM],IEnumOleUndoUnits interface, _ole_ienumoleundounits_next, com.ienumoleundounits_next, ocidl/IEnumOleUndoUnits::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IEnumOleUndoUnits.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOleUndoUnits::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param cElt [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.


### -param rgElt [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>, and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> through each pointer enumerated. If <i>cElt</i> is greater than 1, the caller must also pass a non-NULL pointer passed to <i>pcEltFetched</i> to know how many pointers to release.


### -param pcEltFetched [out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



The caller is responsible for calling the Release method for each element in the array once this method returns successfully. If cUndoUnits is greater than one, the caller must also pass a non-NULL pointer to pcFetched to get the number of pointers it has to release. 



E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the rgpcd array are valid on exit and require no release.




## -see-also




<a href="https://msdn.microsoft.com/f43cbd9d-d91b-4230-816f-693dec7056a4">IEnumOleUndoUnits</a>



<a href="https://msdn.microsoft.com/0822c894-b96c-4b69-94d2-b052dff81f6e">IOleUndoUnit</a>
 

 

