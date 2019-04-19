---
UID: NS:eaptypes._EAP_ATTRIBUTES
title: EAP_ATTRIBUTES (eaptypes.h)
author: windows-sdk-content
description: Contains an array of EAP attributes.
old-location: eaphost\eap_attributes.htm
tech.root: eaphost
ms.assetid: 2f88b475-a4ae-4c40-b0f8-2dd05c676619
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_ATTRIBUTES, EAP_ATTRIBUTES structure [EAPHost], EapAttributes, EapAttributes structure [EAPHost], eaphost.eap_attributes, eaptypes/EAP_ATTRIBUTES, eaptypes/EapAttributes
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
 - EAP_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: EAP_ATTRIBUTES, EapAttributes
req.redist: 
ms.custom: 19H1
---

# EAP_ATTRIBUTES structure


## -description


The <b>EAP_ATTRIBUTES</b> structure contains an array of EAP attributes.


## -struct-fields




### -field dwNumberOfAttributes

The number of <a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a> structures in <b>pAttribs</b>.


### -field pAttribs.size_is

 


### -field pAttribs.size_is.dwNumberOfAttributes

 


### -field pAttribs

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a> structures. The total number of elements is specified in <b>dwNumberOfAttributes</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/a8fe754a-ce6f-45f4-9536-7ffda2183e9e">EAP_ATTRIBUTE</a>
 

 

