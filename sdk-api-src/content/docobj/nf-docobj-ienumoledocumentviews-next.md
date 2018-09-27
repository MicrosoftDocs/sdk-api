---
UID: NF:docobj.IEnumOleDocumentViews.Next
title: IEnumOleDocumentViews::Next
author: windows-sdk-content
description: Retrieves the specified number of items in the enumeration sequence.
old-location: com\ienumoledocumentviews_next.htm
tech.root: com
ms.assetid: a58131bf-88ff-4661-9047-2d70b5e7931b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumOleDocumentViews interface [COM],Next method, IEnumOleDocumentViews.Next, IEnumOleDocumentViews::Next, Next, Next method [COM], Next method [COM],IEnumOleDocumentViews interface, com.ienumoledocumentviews_next, docobj/IEnumOleDocumentViews::Next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
 - DocObj.h
api_name:
 - IEnumOleDocumentViews.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOleDocumentViews::Next


## -description


Retrieves the specified number of items in the enumeration sequence.


## -parameters




### -param cViews [in]

The number of items to be retrieved. If there are fewer than the requested number of items left in the sequence, this method retrieves the remaining elements.

If <i>pcFetched</i> is <b>NULL</b>, this parameter must be 1.


### -param rgpView [out]

An array of enumerated items.

The enumerator is responsible for calling <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>, and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> through each pointer enumerated. If <i>cViews</i> is greater than 1, the caller must also pass a non-<b>NULL</b> pointer passed to <i>pcFetched</i> to know how many pointers to release.


### -param pcFetched [in, out]

The number of items that were retrieved. This parameter is always less than or equal to the number of items requested. This parameter can be <b>NULL</b>, in which case the <i>cViews</i> parameter must be 1.


## -returns



If the method retrieves the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -remarks



E_NOTIMPL is not allowed as a return value. If an error value is returned, no entries in the <i>rgpView</i> array are valid and no calls to Release are required. 




## -see-also




<a href="https://msdn.microsoft.com/cd8fa8b8-17b1-4d77-9611-473725899351">IEnumOleDocumentViews</a>



<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>
 

 

