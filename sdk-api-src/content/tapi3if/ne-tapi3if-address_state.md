---
UID: NE:tapi3if.ADDRESS_STATE
title: ADDRESS_STATE
author: windows-sdk-content
description: The ADDRESS_STATE enum is used by the ITAddress::get_State method to check the address state.
old-location: tapi3\address_state.htm
old-project: Tapi
ms.assetid: 7c79bd68-5f1d-4796-a16b-fd786345cffd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADDRESS_STATE, ADDRESS_STATE enumeration [TAPI 2.2], AS_INSERVICE, AS_OUTOFSERVICE, _tapi3_address_state, tapi3.address_state, tapi3if/ADDRESS_STATE, tapi3if/AS_INSERVICE, tapi3if/AS_OUTOFSERVICE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
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
req.typenames: ADDRESS_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - ADDRESS_STATE
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ADDRESS_STATE enumeration


## -description


The 
<b>ADDRESS_STATE</b> enum is used by the 
<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">ITAddress::get_State</a> method to check the address state.


## -enum-fields




### -field AS_INSERVICE

Normal state; the address can be used.


### -field AS_OUTOFSERVICE

The address is temporarily out of service, but may go back into service at some time.


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">ITAddress::get_State</a>
 

 

