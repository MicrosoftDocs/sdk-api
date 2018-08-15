---
UID: NF:elscore.MappingRecognizeText
title: MappingRecognizeText function
author: windows-sdk-content
description: Calls upon an ELS service to recognize text. For example, the Microsoft Language Detection service will attempt to recognize the language in which the input text is written.
old-location: intl\mappingrecognizetext.htm
old-project: Intl
ms.assetid: 49f30bdd-4612-423b-9913-9c35ad8a88d5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MappingRecognizeText, MappingRecognizeText function [Internationalization for Windows Applications], elscore/MappingRecognizeText, intl.mappingrecognizetext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: elscore.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, *PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Elscore.dll
 - ext-ms-win-els-elscore-l1-1-0.dll
api_name:
 - MappingRecognizeText
product: Windows
targetos: Windows
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# MappingRecognizeText function


## -description


Calls upon an ELS service to recognize text. For example, the Microsoft Language Detection service will attempt to recognize the language in which the input text is written.


## -parameters




### -param pServiceInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a> structure containing information about the service to use in text recognition. The structure must be one of the structures retrieved by a previous call to <a href="https://msdn.microsoft.com/6d02e085-405e-4388-bf2f-409c92a7b190">MappingGetServices</a>. This parameter cannot be set to <b>NULL</b>.


### -param pszText [in]

Pointer to the text to recognize. The text must be UTF-16, but some services have additional requirements for the input format. This parameter cannot be set to <b>NULL</b>.


### -param dwLength [in]

Length, in characters, of the text specified in <i>pszText</i>.


### -param dwIndex [in]

Index inside the specified text to be used by the service. This value should be between 0 and <i>dwLength</i>-1. If the application wants to process the entire text, it should set this parameter to 0.


### -param pOptions [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a> structure containing options that affect the result and behavior of text recognition. The application does not have to specify values for all structure members. This parameter can be set to <b>NULL</b> to use the default mapping options.


### -param pbag [in, out]

Pointer to a <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure in which the service stores its results. On input, the application passes a structure with only the size provided, and the other members set to 0. On output, the structure is filled with information produced by the service during text recognition. This parameter cannot be set to <b>NULL</b>.


## -returns



Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.




## -remarks



The type of text to recognize depends on the service type used by the application. For more information, see <a href="https://msdn.microsoft.com/9db9045d-b289-4c6c-9b17-ddbc2c1d3089">Requesting Text Recognition</a>.

<div class="alert"><b>Warning</b>  The data referred to by <i>pszText</i> and <i>pOptions</i> must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="https://msdn.microsoft.com/7e06e85d-109a-4c5f-be18-3750e25c4986">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <a href="https://msdn.microsoft.com/c3903d10-3429-4707-82b5-33efa6b2dc4c">MappingDoAction</a> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a>



<a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a>



<a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/9db9045d-b289-4c6c-9b17-ddbc2c1d3089">Requesting Text Recognition</a>
 

 

