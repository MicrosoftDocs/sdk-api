---
UID: NF:elscore.MappingDoAction
title: MappingDoAction function
author: windows-sdk-content
description: Causes an ELS service to perform an action after text recognition has occurred. For example, a phone dialer service first must recognize phone numbers and then can perform the &#0034;action&#0034; of dialing a number.
old-location: intl\mappingdoaction.htm
tech.root: Intl
ms.assetid: c3903d10-3429-4707-82b5-33efa6b2dc4c
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: MappingDoAction, MappingDoAction function [Internationalization for Windows Applications], elscore/MappingDoAction, intl.mappingdoaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Elscore.dll
api_name:
 - MappingDoAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MappingDoAction function


## -description


Causes an ELS service to perform an action after text recognition has occurred. For example, a phone dialer service first must recognize phone numbers and then can perform the "action" of dialing a number.


## -parameters




### -param pBag [in, out]

Pointer to a <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure containing the results of a previous call to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>. This parameter cannot be set to <b>NULL</b>.


### -param dwRangeIndex [in]

A starting index inside the text recognition results for a recognized text range. This value should be between 0 and the range count.


### -param pszActionId [in]

Pointer to the identifier of the action to perform. This parameter cannot be set to <b>NULL</b>.


## -returns



Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.




## -remarks



The application must precede the call to <b>MappingDoAction</b> with a call to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.

<div class="alert"><b>Warning</b>  The data referred to by the <i>pszText</i> and <i>pOptions</i> arguments passed to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> 

must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="https://msdn.microsoft.com/7e06e85d-109a-4c5f-be18-3750e25c4986">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <b>MappingDoAction</b> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a>



<a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>
 

 

