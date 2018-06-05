---
UID: NF:mediaobj.IEnumDMO.Skip
title: IEnumDMO::Skip
author: windows-sdk-content
description: The Skip method skips over a specified number of items in the enumeration sequence.
old-location: dshow\ienumdmo_skip.htm
old-project: DirectShow
ms.assetid: 32722190-52b5-468a-91d6-a828ad02b203
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IEnumDMO interface [DirectShow],Skip method, IEnumDMO.Skip, IEnumDMO::Skip, IEnumDMOSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumDMO interface, dshow.ienumdmo_skip, mediaobj/IEnumDMO::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IEnumDMO.Skip
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IEnumDMO::Skip


## -description



The <code>Skip</code> method skips over a specified number of items in the enumeration sequence.




## -parameters




### -param cItemsToSkip

Number of items to skip.


## -returns



Returns S_OK if the number items skipped equals <i>cItemsToSkip</i>. Otherwise, returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/221248f2-5c8f-442e-a6ad-e0372ddc1aae">IEnumDMO Interface</a>
 

 

