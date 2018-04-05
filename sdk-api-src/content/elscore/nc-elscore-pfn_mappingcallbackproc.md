---
UID: NC:elscore.PFN_MAPPINGCALLBACKPROC
title: PFN_MAPPINGCALLBACKPROC
author: windows-driver-content
description: An application-defined callback function that asynchronously processes data produced by the MappingRecognizeText function.
old-location: intl\mappingcallbackproc.htm
old-project: Intl
ms.assetid: 7a324708-4f1b-467c-af1a-da36d1f7eba0
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MappingCallbackProc, MappingCallbackProc callback function [Internationalization for Windows Applications], PFN_MAPPINGCALLBACKPROC, elscore/MappingCallbackProc, intl.mappingcallbackproc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, *PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Elscore.h
api_name:
-	MappingCallbackProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PFN_MAPPINGCALLBACKPROC callback


## -description


An application-defined callback function that asynchronously processes data produced by the <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> function. The <b>MAPPINGCALLBACKPROC</b> type defines a pointer to this callback function. <b>MappingCallbackProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param *pBag [in]

Pointer to a <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure containing the results of the call to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>.


### -param data [in]

Pointer to private application data. This pointer is the same as that passed in the <b>pRecognizeCallerData</b> member of the <a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a> structure.


### -param dwDataSize [in]

Size, in bytes, of the private application data. This size is the same as that passed in the <b>dwRecognizeCallerDataSize</b> member of the <a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a> structure when the application calls <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> asynchronuously.


### -param Result [in]

Return code from <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>. The return code is S_OK if the function succeeded, or an error code otherwise.


## -returns



This callback function does not return a value.




## -remarks



A <b>MappingCallbackProc</b> function consumes the results retrieved by <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>. The application registers the callback function by passing its address to <a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a> in a <a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a> structure.

The application should check the <i>Result</i> parameter before using the data in the <i>pBag</i> parameter. When it is done using the data from the property bag, the application must call <a href="https://msdn.microsoft.com/7e06e85d-109a-4c5f-be18-3750e25c4986">MappingFreePropertyBag</a> because the property bag can contain pointers into the original text. For more information about the property bag, see the remarks for the <a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/228625b3-928c-451f-9a3f-7eb3130ac622">MAPPING_OPTIONS</a>



<a href="https://msdn.microsoft.com/08e55e27-5118-40ea-b973-cea0b1c263da">MAPPING_PROPERTY_BAG</a>



<a href="https://msdn.microsoft.com/49f30bdd-4612-423b-9913-9c35ad8a88d5">MappingRecognizeText</a>



<a href="https://msdn.microsoft.com/48609c55-9e82-4407-ae28-41b07b1e1161">Providing Callbacks for ELS Services</a>
 

 

