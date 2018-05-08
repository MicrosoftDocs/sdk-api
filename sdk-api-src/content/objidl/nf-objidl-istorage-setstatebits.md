---
UID: NF:objidl.IStorage.SetStateBits
title: IStorage::SetStateBits
author: windows-driver-content
description: The SetStateBits method stores up to 32 bits of state information in this storage object.
old-location: stg\istorage_setstatebits.htm
old-project: Stg
ms.assetid: 52606df8-10ea-40e7-bb61-c86c7b7262d2
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IStorage interface [Structured Storage],SetStateBits method, IStorage.SetStateBits, IStorage::SetStateBits, SetStateBits, SetStateBits method [Structured Storage], SetStateBits method [Structured Storage],IStorage interface, _stg_istorage_setstatebits, objidl/IStorage::SetStateBits, stg.istorage_setstatebits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IStorage.SetStateBits
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStorage::SetStateBits


## -description


The <b>SetStateBits</b> method stores up to 32 bits of state information in this storage object. This method is reserved for future use.


## -parameters




### -param grfStateBits [in]

Specifies the new values of the bits to set. No legal values are defined for these bits; they are all reserved for future use and must not be used by applications.


### -param grfMask [in]

A binary mask indicating which bits in <i>grfStateBits</i> are significant in this call.


## -returns



This method can return one of these values.




## -remarks



The values for the state bits are not currently defined.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

