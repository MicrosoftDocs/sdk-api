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

# OLECMDTEXTF enumeration


## -description


Specifies the type of information that an object should store in the <a href="https://msdn.microsoft.com/c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e">OLECMDTEXT</a> structure passed in <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>. One value from this enumeration is stored the <b>cmdtextf</b> member of the <b>OLECMDTEXT</b> structure to indicate the desired information.




## -enum-fields




### -field OLECMDTEXTF_NONE

No extra information is requested.


### -field OLECMDTEXTF_NAME

The object should provide the localized name of the command.


### -field OLECMDTEXTF_STATUS

The object should provide a localized status string for the command.


## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e">OLECMDTEXT</a>
 

 

