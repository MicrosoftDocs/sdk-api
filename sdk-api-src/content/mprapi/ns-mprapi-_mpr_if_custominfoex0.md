---
UID: NS:mprapi._MPR_IF_CUSTOMINFOEX0
title: "_MPR_IF_CUSTOMINFOEX0"
author: windows-sdk-content
description: Gets or sets tunnel specific custom configuration for a demand dial interfaces.
old-location: rras\mpr_if_custominfoex0.htm
tech.root: rras
ms.assetid: 53c4b7ae-db73-4d97-a99f-a98354c48a92
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PMPR_IF_CUSTOMINFOEX0, MPRAPI_IF_CUSTOM_CONFIG_FOR_IKEV2, MPR_IF_CUSTOMINFOEX0, MPR_IF_CUSTOMINFOEX0 structure [RAS], PMPR_IF_CUSTOMINFOEX0, PMPR_IF_CUSTOMINFOEX0 structure pointer [RAS], _MPR_IF_CUSTOMINFOEX0, mprapi/MPR_IF_CUSTOMINFOEX0, mprapi/PMPR_IF_CUSTOMINFOEX0, rras.mpr_if_custominfoex0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - mprapi.h
api_name:
 - MPR_IF_CUSTOMINFOEX0
product: Windows
targetos: Windows
req.typenames: MPR_IF_CUSTOMINFOEX0, *PMPR_IF_CUSTOMINFOEX0
req.redist: 
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
 

 

