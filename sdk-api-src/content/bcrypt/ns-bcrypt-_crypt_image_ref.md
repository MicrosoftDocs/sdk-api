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

# _CRYPT_IMAGE_REF structure


## -description


The <b>CRYPT_IMAGE_REF</b> structure contains information about a CNG provider module.


## -struct-fields




### -field pszImage

A pointer to a null-terminated Unicode string that contains the name of the provider module.


### -field dwFlags

A set of flags that indicate how CNG will manage the binary image with respect to this interface. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MIN_DEPENDENCIES"></a><a id="crypt_min_dependencies"></a><dl>
<dt><b>CRYPT_MIN_DEPENDENCIES</b></dt>
</dl>
</td>
<td width="60%">
The provider for this interface is only dependent on a minimum set of system components.  This flag applies to a specific interface only and does not mean that all interfaces supported by the binary image conform to this standard.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_PROCESS_ISOLATE"></a><a id="crypt_process_isolate"></a><dl>
<dt><b>CRYPT_PROCESS_ISOLATE</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/cf30f635-4918-4911-9db0-df90d26a2f1a">BCryptResolveProviders</a>



<a href="https://msdn.microsoft.com/3bd4a07c-8b80-4bbc-9922-88ea007f6ccd">CRYPT_PROVIDER_REF</a>
 

 

