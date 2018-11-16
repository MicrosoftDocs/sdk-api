---
UID: NF:imapi2.IDiscFormat2Erase.put_FullErase
title: IDiscFormat2Erase::put_FullErase
author: windows-sdk-content
description: Determines the quality of the disc erasure.
old-location: imapi\idiscformat2erase_put_fullerase.htm
tech.root: imapi
ms.assetid: 9a76ebbe-69c5-46a4-b620-220957220e53
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],put_FullErase method, IDiscFormat2Erase.put_FullErase, IDiscFormat2Erase::put_FullErase, imapi.idiscformat2erase_put_fullerase, imapi2/IDiscFormat2Erase::put_FullErase, put_FullErase, put_FullErase method [IMAPI], put_FullErase method [IMAPI],IDiscFormat2Erase interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2Erase.put_FullErase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IDiscFormat2Erase.put_FullErase
: 
---

# IDiscFormat2Erase::put_FullErase


## -description


Determines the quality of the disc erasure.


## -parameters




### -param value [in]

Set to VARIANT_TRUE to fully erase the disc by overwriting the  entire medium at least once. 

Set to VARIANT_FALSE to overwrite the directory tracks, but not the entire disc. This option requires less time to perform than the full erase option. 

The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/3789c876-f42c-4f69-b683-96c157d6418d">IDiscFormat2Erase</a>



<a href="https://msdn.microsoft.com/dc71d1bf-b068-42c0-a87d-ae8fac279a58">IDiscFormat2Erase::EraseMedia</a>



<a href="https://msdn.microsoft.com/56b4db17-1699-4e09-9a6d-ef5e998621c5">IDiscFormat2Erase::get_FullErase</a>
 

 

