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

# PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback function


## -description


The <b>CertEnumSystemStoreLocationCallback</b> 
	callback function formats and presents information on each system store location found by a call to 
	<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>.


## -parameters




### -param pwszStoreLocation [in]

String that contains information on the store location found.


### -param dwFlags [in]

Flag used to call for an alteration of the presentation.


### -param *pvReserved [in]

Reserved for future use.


### -param *pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> 
	 passed to <a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.



