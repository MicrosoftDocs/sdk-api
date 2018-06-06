---
UID: NF:comcat.IEnumGUID.Skip
title: IEnumGUID::Skip
author: windows-sdk-content
description: Skips over the specified number of items in the enumeration sequence.
old-location: com\ienumguid_skip.htm
old-project: com
ms.assetid: 8c3b955b-ba36-4bab-af89-fc89e08e6e94
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumGUID interface [COM],Skip method, IEnumGUID.Skip, IEnumGUID::Skip, Skip, Skip method [COM], Skip method [COM],IEnumGUID interface, _com_ienumguid_skip, com.ienumguid_skip, comcat/IEnumGUID::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ServerInformation, *PServerInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumGUID.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumGUID::Skip


## -description


Skips over the specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

The number of items to be skipped.


## -returns



If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/4f2e0f96-a471-4883-be41-d93806461020">IEnumGUID</a>
 

 

