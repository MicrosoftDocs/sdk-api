---
UID: NF:objidl.IEnumContextProps.Skip
title: IEnumContextProps::Skip
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienumcontextprops_skip.htm
old-project: com
ms.assetid: 22c50b48-a6e2-4153-9604-57f07512d4ce
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumContextProps interface [COM],Skip method, IEnumContextProps.Skip, IEnumContextProps::Skip, Skip, Skip method [COM], Skip method [COM],IEnumContextProps interface, _com_ienumcontextprops_skip, com.ienumcontextprops_skip, objidlbase/IEnumContextProps::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IEnumContextProps.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IEnumContextProps::Skip


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a>
 

 

