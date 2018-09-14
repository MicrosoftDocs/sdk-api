---
UID: NS:eaptypes._EAP_METHOD_INFO_ARRAY
title: "_EAP_METHOD_INFO_ARRAY"
author: windows-sdk-content
description: Contains information on EAP methods installed on the client computer.
old-location: eaphost\eap_method_info_array.htm
tech.root: EAPHost
ms.assetid: a3e2d5c0-eacd-46de-b092-6fd749870881
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EAP_METHOD_INFO_ARRAY, EAP_METHOD_INFO_ARRAY structure [EAPHost], PEAP_METHOD_INFO_ARRAY, PEAP_METHOD_INFO_ARRAY structure pointer [EAPHost], _EAP_METHOD_INFO_ARRAY, eaphost.eap_method_info_array, eaptypes/EAP_METHOD_INFO_ARRAY, eaptypes/PEAP_METHOD_INFO_ARRAY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_METHOD_INFO_ARRAY
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_INFO_ARRAY
req.redist: 
---

# _EAP_METHOD_INFO_ARRAY structure


## -description


The <b>EAP_METHOD_INFO_ARRAY</b> structure contains information on EAP methods installed on the client computer. After populating <b>EAP_METHOD_INFO_ARRAY</b>, EAPHost passes this method information to the supplicant.


## -struct-fields




### -field dwNumberOfMethods

The number of <a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a> structures in <b>pEapMethods</b>.


### -field pEapMethods

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a> structures. The total number of elements is specified in <b>dwNumberOfMethods</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/10407b85-5d2c-4c75-9b65-a0d65d4cc7ab">EAP Method Properties</a>



<a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a>



<a href="https://msdn.microsoft.com/3deb04da-3071-4ddd-a7cb-82a1c47c3677">EAP_METHOD_INFO_ARRAY_EX</a>



<a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a>



<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a>
 

 

