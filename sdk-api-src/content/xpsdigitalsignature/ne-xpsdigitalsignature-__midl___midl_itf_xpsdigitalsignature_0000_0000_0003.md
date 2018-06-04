---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_xpsdigitalsignature_0000_0000_0003 enumeration


## -description


Specifies whether markup compatibility detection must be run 
before signing.


## -enum-fields




### -field XPS_SIGN_FLAGS_NONE

The system will check for any markup compatibility elements before 
signing the package. If any markup compatibility elements are found, the signing operation 
fails with an <b>XPS_E_MARKUP_COMPATIBILITY_ELEMENTS</b> error.


### -field XPS_SIGN_FLAGS_IGNORE_MARKUP_COMPATIBILITY

The system will not check for any markup compatibility elements before 
signing the package.


## -see-also




<a href="https://msdn.microsoft.com/02d07300-e8f2-44fa-a562-5cec03af9a8c">IXpsSigningOptions::GetFlags</a>



<a href="https://msdn.microsoft.com/59467fd5-c462-4827-a4f8-e152df981ace">IXpsSigningOptions::SetFlags</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=123375">Standard ECMA-376, Office Open XML File Formats</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

