---
UID: NS:eaptypes._EAP_METHOD_INFO_EX
title: "_EAP_METHOD_INFO_EX"
author: windows-sdk-content
description: Contains information about an EAP method.
old-location: eaphost\eap_method_info_ex.htm
old-project: eaphost
ms.assetid: 2d25f418-2130-4f9c-b3f4-f639dfba020a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EAP_METHOD_INFO_EX, EAP_METHOD_INFO_EX structure [EAPHost], _EAP_METHOD_INFO_EX, eaphost.eap_method_info_ex, eaptypes/EAP_METHOD_INFO_EX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
tech.root: 
req.typenames: EAP_METHOD_INFO_EX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_METHOD_INFO_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EAP_METHOD_INFO_EX structure


## -description


 The <b>EAP_METHOD_INFO_EX</b> structure contains  information about an EAP method.


## -struct-fields




### -field eaptype

 


### -field pwszAuthorName

Pointer to a zero-terminated Unicode string that contains the name of the EAP method's author.


### -field pwszFriendlyName

Pointer to a zero-terminated Unicode string that contains the display name of the EAP method.


### -field eapProperties

Set of flags that describe specific properties of the EAP methods. For flag descriptions, see <a href="https://msdn.microsoft.com/10407b85-5d2c-4c75-9b65-a0d65d4cc7ab">EAP Method Properties</a>.


### -field pInnerMethodInfoArray

Pointer to an <a href="https://msdn.microsoft.com/3deb04da-3071-4ddd-a7cb-82a1c47c3677">EAP_METHOD_INFO_ARRAY_EX</a> structure that contains information about all of the EAP methods installed on the client computer.


#### - eapType

An <a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a> structure that identifies the EAP method.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/10407b85-5d2c-4c75-9b65-a0d65d4cc7ab">EAP Method Properties</a>



<a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a>



<a href="https://msdn.microsoft.com/a3e2d5c0-eacd-46de-b092-6fd749870881">EAP_METHOD_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/3deb04da-3071-4ddd-a7cb-82a1c47c3677">EAP_METHOD_INFO_ARRAY_EX</a>



<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a>
 

 

