---
UID: NS:elscore._MAPPING_OPTIONS
title: "_MAPPING_OPTIONS"
author: windows-sdk-content
description: Contains options for text recognition. The values stored in this structure affect the behavior and results of MappingRecognizeText.
old-location: intl\mappingoptions.htm
old-project: Intl
ms.assetid: 228625b3-928c-451f-9a3f-7eb3130ac622
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PMAPPING_OPTIONS, MAPPING_OPTIONS, MAPPING_OPTIONS structure [Internationalization for Windows Applications], PMAPPING_OPTIONS, PMAPPING_OPTIONS structure pointer [Internationalization for Windows Applications], _MAPPING_OPTIONS, elscore/MAPPING_OPTIONS, elscore/PMAPPING_OPTIONS, intl.mappingoptions"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MAPPING_OPTIONS, *PMAPPING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Elscore.h
api_name:
-	MAPPING_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _MAPPING_OPTIONS structure


## -description



Contains options for text recognition. The values stored in this structure affect the behavior and results of <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.




## -struct-fields




### -field Size

Size of the structure, used to validate the structure version. This value is required.


### -field pszInputLanguage

Optional. Pointer to an input language string, following the IETF naming convention, that identifies the input language that the service should be able to accept. The application can set this member to <b>NULL</b> to indicate that the service is free to interpret the input as any input language it supports.


### -field pszOutputLanguage

Optional. Pointer to an output language string, following the IETF naming convention, that identifies the output language that the service should be able to use to produce results. The application can set this member to <b>NULL</b> if the service should decide the output language.
			 


### -field pszInputScript

Optional. Pointer to a standard Unicode script name that should be accepted by the service. The application can set this member to <b>NULL</b> to let the service decide how handle the input.


### -field pszOutputScript

Optional. Pointer to a standard Unicode script name that the service should use to retrieve results. The application can set this member to <b>NULL</b> to let the service decide the output script.


### -field pszInputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format that the service should be able to interpret when the application passes data. Examples of content types are "text/plain", "text/html", and "text/css". The application can set this member to <b>NULL</b> to indicate the "text/plain" content type. 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content type specification can be found at <a href="http://go.microsoft.com/fwlink/p/?linkid=161570">Text Media Types</a>.</div>
<div> </div>

### -field pszOutputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format in which the service should retrieve data. The application can set this member to <b>NULL</b> to let the service decide the output content type.


### -field pszUILanguage

Reserved.


### -field pfnRecognizeCallback

Optional. Pointer to an application callback function to receive callbacks with the results from the <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> function. If a callback function is specified, text recognition is executed in asynchronous mode and the application obtains results through the callback function. The application must set this member to <b>NULL</b> if text recognition is to be synchronous. 
			  


### -field pRecognizeCallerData

Optional. Pointer to private application data passed to the callback function by a service after text recognition is complete. The application must set this member to <b>NULL</b> to indicate no private application data.


### -field dwRecognizeCallerDataSize

Optional. Size, in bytes, of any private application data indicated by the <b>pRecognizeCallerData</b> member.


### -field pfnActionCallback

Reserved.


### -field pActionCallerData

Reserved.


### -field dwActionCallerDataSize

Reserved.


### -field dwServiceFlag

Optional. Private flag that a service provider defines to affect service behavior. Services can interpret this flag as they require.

<div class="alert"><b>Note</b>  For Windows 7, none of the available ELS services support flags.</div>
<div> </div>

### -field GetActionDisplayName

Reserved.


## -remarks



The application does not have to fill in all members of this structure, as services treat <b>NULL</b> members as default values. All unused members must be set to 0.

<div class="alert"><b>Warning</b>  The data passed in this structure to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>, as well as data referred to by the <i>pszText</i> argument in that call, 

must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="https://msdn.microsoft.com/7e06e85d-109a-4c5f-be18-3750e25c4986">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <a href="https://msdn.microsoft.com/c3903d10-3429-4707-82b5-33efa6b2dc4c">MappingDoAction</a> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/58cdccf8-f052-4bb3-9391-2cc537d820dd">Extended Linguistic Services Structures</a>



<a href="https://msdn.microsoft.com/adff7901-1903-45dd-888f-1b8c5bb05de1">MAPPING_DATA_RANGE</a>



<a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>
 

 

