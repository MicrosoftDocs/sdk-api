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

# MBN_PROVIDER structure


## -description


The <b>MBN_PROVIDER</b> structure represents a network service provider.  It is used by many of the provider-specific methods of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.


## -struct-fields




### -field providerID

Contains the provider ID.  For GSM networks, this string is a concatenation of a 3-digit mobile country code (MCC) and a 2- or 3-digit mobile network code (MNC).  For CDMA networks, this string is a 5-digit SID.  The maximum length of this string is defined by <b>MBN_PROVIDERID_LEN</b> from <a href="https://msdn.microsoft.com/1cfe230c-16b5-490d-938f-604489a4a936">MBN_PROVIDER_CONSTANTS</a>.  The caller must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


### -field providerState

Contains a bitwise OR combination of <a href="https://msdn.microsoft.com/c9bbda5d-96bc-410c-afac-eba3e5bd23ee">MBN_PROVIDER_STATE</a> values that represent the provider state.


### -field providerName

Contains the provider name.  The contents of this member should be ignored when setting the preferred provider list.  The maximum length of this string is defined by <b>MBN_PROVIDERNAME_LEN</b> from <a href="https://msdn.microsoft.com/1cfe230c-16b5-490d-938f-604489a4a936">MBN_PROVIDER_CONSTANTS</a>.  The string can be empty.  The caller must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.  


### -field dataClass

Contains a bitwise OR combination of <a href="https://msdn.microsoft.com/798d5d72-9267-433f-b890-9302a0a600f2">MBN_DATA_CLASS</a> values that indicate which data services are applicable or available for transfer.  This member should be ignored when queried for the home provider.


## -see-also




<a href="https://msdn.microsoft.com/9D681192-1E40-4314-8E7F-8934AA8162D3">MBN_PROVIDER2</a>
 

 

