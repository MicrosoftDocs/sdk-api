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

# CMSPCallMultiGraph::Init


## -description


The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>) to initialize the MSP call object. The 
<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a> implementation initializes its members using the passed-in information. It calls 
<a href="https://msdn.microsoft.com/74a68851-f1c2-41ed-94cd-ec043be0f0d1">MSPAddressAddRef</a> on the MSP address object. Derived MSPs will want to override this method and call it in the overridden method; the overridden method should create the default streams based on the passed-in media types.


## -parameters




### -param pMSPAddress

Pointer to 
<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a> for call being initialized.


### -param htCall

The MSP's handle for the call being initialized


### -param dwReserved

Reserved parameter.


### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types of call.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

