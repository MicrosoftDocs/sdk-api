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

# _MPR_IF_CUSTOMINFOEX0 structure


## -description


Gets or sets tunnel specific custom configuration for a demand dial interfaces.

Do not use the <b>MPR_IF_CUSTOMINFOEX0</b> structure directly in your code; using <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">MPR_IF_CUSTOMINFOEX</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/2f4e1ddc-7991-4091-9889-fdd2d75e702f">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>MPR_IF_CUSTOMINFOEX0</b> structure. 


### -field dwFlags

A value that specifies the tunnel type for which the custom configuration is available. The following values are supported.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
No custom configuration available.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2_"></a><a id="mprapi_if_custom_config_for_ikev2_"></a><dl>
<dt><b>MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2 </b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
IKEv2 tunnel specific configuration is available.

</td>
</tr>
</table>
 


### -field customIkev2Config

A <a href="https://msdn.microsoft.com/c81611c6-3bad-4965-b4fb-b2c8074cee28">ROUTER_IKEv2_IF_CUSTOM_CONFIG0</a> structure that specifies the IKEv2 tunnel configuration parameters.  


## -see-also




<a href="https://msdn.microsoft.com/01974ac8-dffc-4564-bac1-68ac0437d22b">MprAdminInterfaceGetCustomInfoEx</a>



<a href="https://msdn.microsoft.com/306d9d6c-6196-4a1f-8549-f8dd0fb5ab6f">MprAdminInterfaceSetCustomInfoEx</a>



<a href="https://msdn.microsoft.com/97fa62f4-5e1c-4634-a3c7-974425717080">MprConfigInterfaceGetCustomInfoEx</a>



<a href="https://msdn.microsoft.com/fff18156-ba94-45b7-86c2-a604823a9b08">MprConfigInterfaceSetCustomInfoEx</a>
 

 

