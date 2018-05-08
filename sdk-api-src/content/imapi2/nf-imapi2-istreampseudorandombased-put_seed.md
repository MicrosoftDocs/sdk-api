---
UID: NF:imapi2.IStreamPseudoRandomBased.put_Seed
title: IStreamPseudoRandomBased::put_Seed
author: windows-driver-content
description: Sets the seed value used by the random number generator and seeks to the start of stream.
old-location: imapi\istreampseudorandombased_put_seed.htm
old-project: imapi
ms.assetid: 455d087d-a6f5-45ab-9c0d-c46e721cba6e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],put_Seed method, IStreamPseudoRandomBased.put_Seed, IStreamPseudoRandomBased::put_Seed, imapi.istreampseudorandombased_put_seed, imapi2/IStreamPseudoRandomBased::put_Seed, put_Seed, put_Seed method [IMAPI], put_Seed method [IMAPI],IStreamPseudoRandomBased interface
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IStreamPseudoRandomBased.put_Seed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamPseudoRandomBased::put_Seed


## -description


Sets the seed value used by the random number generator and seeks to the start of stream.


## -parameters




### -param value [in]

Seed value for the random number generator.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -see-also




<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>



<a href="https://msdn.microsoft.com/c5362760-84c6-4e93-b3cd-2ce568b13102">IStreamPseudoRandomBased::get_Seed</a>



<a href="https://msdn.microsoft.com/a6edf21f-b89a-4780-8065-4d09758fe701">IStreamPseudoRandomBased::put_ExtendedSeed</a>
 

 

