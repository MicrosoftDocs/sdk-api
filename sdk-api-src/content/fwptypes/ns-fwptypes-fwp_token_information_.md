---
UID: NS:fwptypes.FWP_TOKEN_INFORMATION_
title: FWP_TOKEN_INFORMATION_
author: windows-sdk-content
description: The FWP_TOKEN_INFORMATION structure defines a set of security identifiers that are used for user-mode classification.
old-location: netvista\fwp_token_information.htm
tech.root: NetVista
ms.assetid: e30a5441-3f36-4da9-a066-9937a484de84
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_TOKEN_INFORMATION, FWP_TOKEN_INFORMATION structure [Network Drivers Starting with Windows Vista], FWP_TOKEN_INFORMATION_, fwptypes/FWP_TOKEN_INFORMATION, netvista.fwp_token_information, wfp_ref_3_struct_1_top_fwp_A-Z_1026929a-bdaa-49f7-9d11-e5bba3174348.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_TOKEN_INFORMATION
product: Windows
targetos: Windows
req.typenames: FWP_TOKEN_INFORMATION
req.redist: 
---

# FWP_TOKEN_INFORMATION_ structure


## -description


The <b>FWP_TOKEN_INFORMATION</b> structure defines a set of security identifiers that are used for user-mode
  classification.


## -struct-fields




### -field sidCount

The number of <a href="https://msdn.microsoft.com/37c299ab-16a6-4fa2-8ac9-55d75cc98f60">SID_AND_ATTRIBUTES</a> structures in the array pointed to by the 
     <b>sids</b> member.


### -field sids

An array of <a href="https://msdn.microsoft.com/37c299ab-16a6-4fa2-8ac9-55d75cc98f60">SID_AND_ATTRIBUTES</a> structures. Each structure represents a security
     identifier and its attributes.


### -field restrictedSidCount

The number of <a href="https://msdn.microsoft.com/37c299ab-16a6-4fa2-8ac9-55d75cc98f60">SID_AND_ATTRIBUTES</a> structures in the array pointed to by the 
     <b>restrictedSids</b> member.


### -field restrictedSids

An array of <a href="https://msdn.microsoft.com/37c299ab-16a6-4fa2-8ac9-55d75cc98f60">SID_AND_ATTRIBUTES</a> structures. Each structure represents a security
     identifier and its attributes.


## -remarks



The <b>FWP_TOKEN_INFORMATION</b> structure is used for user-mode classification. This structure is not used
    by callout drivers.




## -see-also




<a href="https://msdn.microsoft.com/7632d9be-dd16-40d2-b7b4-2d4efb6aaa99">FWP_DATA_TYPE</a>
 

 

