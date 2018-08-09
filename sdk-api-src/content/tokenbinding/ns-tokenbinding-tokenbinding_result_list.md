---
UID: NS:tokenbinding.TOKENBINDING_RESULT_LIST
title: TOKENBINDING_RESULT_LIST
author: windows-sdk-content
description: Contains the results for each of the token bindings that TokenBindingVerifyMessage verified.
old-location: security\tokenbinding_result_list.htm
old-project: seccng
ms.assetid: D14CBEA3-5F46-4C45-8C11-407D6E70FD56
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TOKENBINDING_RESULT_LIST, TOKENBINDING_RESULT_LIST structure [Security], security.tokenbinding_result_list, tokenbinding/TOKENBINDING_RESULT_LIST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: TOKENBINDING_RESULT_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_RESULT_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TOKENBINDING_RESULT_LIST structure


## -description


Contains the results for each of the token bindings that <a href="https://msdn.microsoft.com/D6827DA3-75DC-4F31-B57A-4ED5B5F03112">TokenBindingVerifyMessage</a>   verified.


## -struct-fields




### -field resultCount

The number of elements in the array that  the <b>resultData</b> member contains.


### -field resultData

An array of results, one for each of the token bindings that <a href="https://msdn.microsoft.com/D6827DA3-75DC-4F31-B57A-4ED5B5F03112">TokenBindingVerifyMessage</a>   verified.


## -see-also




<a href="https://msdn.microsoft.com/D6827DA3-75DC-4F31-B57A-4ED5B5F03112">TokenBindingVerifyMessage</a>
 

 

