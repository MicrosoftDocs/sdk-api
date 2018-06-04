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

# FAX_PRIORITY_TYPE_ENUM enumeration


## -description


The <b>FAX_PRIORITY_TYPE_ENUM</b> enumeration defines the types of priorities for outbound faxes.


## -enum-fields




### -field fptLOW

The fax will be sent with a low priority. All faxes that have a normal or a high priority will be sent before a fax that has a low priority.


### -field fptNORMAL

The fax will be sent with a normal priority. All faxes that have a high priority will be sent before a fax that has a normal priority.


### -field fptHIGH

The fax will be sent with a high priority.


## -see-also




<a href="https://msdn.microsoft.com/4f7ebcad-ff7d-4c11-b4c4-c7325415231e">IFaxDocument::get_Priority</a>



<a href="https://msdn.microsoft.com/0cf5d46f-0c26-4fa5-808e-13bdf1901964">IFaxOutgoingJob::get_Priority</a>



<a href="https://msdn.microsoft.com/bd727334-0e7a-4f2b-a4bb-2308c9ecfc9a">IFaxOutgoingMessage::get_Priority</a>
 

 

