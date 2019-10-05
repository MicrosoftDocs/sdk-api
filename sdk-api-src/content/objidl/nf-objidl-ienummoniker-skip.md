---
UID: NF:objidl.IEnumMoniker.Skip
title: IEnumMoniker::Skip (objidl.h)
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienummoniker_skip.htm
tech.root: com
ms.assetid: 90df5bc4-6bb0-44bf-b675-d4a93d4680ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumMoniker interface [COM],Skip method, IEnumMoniker.Skip, IEnumMoniker::Skip, Skip, Skip method [COM], Skip method [COM],IEnumMoniker interface, _ole_ienummoniker_skip, com.ienummoniker_skip, objidl/IEnumMoniker::Skip
ms.topic: method
f1_keywords: 
 - "objidl/IEnumMoniker.Skip"
dev_langs:
 - c++
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
 - IEnumMoniker.Skip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumMoniker::Skip


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a>
 

 

