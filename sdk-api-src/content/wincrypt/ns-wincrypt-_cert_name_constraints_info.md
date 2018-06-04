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

# _CERT_NAME_CONSTRAINTS_INFO structure


## -description


The <b>CERT_NAME_CONSTRAINTS_INFO</b> structure contains information about certificates that are specifically permitted or excluded from trust.


## -struct-fields




### -field cPermittedSubtree

<b>DWORD</b> indicating the number of subtrees in the <b>rgPermittedSubtree</b> array.


### -field rgPermittedSubtree

Array of 
<a href="https://msdn.microsoft.com/991e277c-46f5-4987-ab48-0d1c1442273f">CERT_GENERAL_SUBTREE</a> structures, each identifying a permitted certificate name.


### -field cExcludedSubtree

<b>DWORD</b> indicating the number of subtrees in the <b>rgExcludedSubtree</b> array.


### -field rgExcludedSubtree

Array of <a href="https://msdn.microsoft.com/991e277c-46f5-4987-ab48-0d1c1442273f">CERT_GENERAL_SUBTREE</a> structures, each identifying an excluded certificate name.

