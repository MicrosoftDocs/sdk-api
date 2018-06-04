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

# tagDATADIR enumeration


## -description


Specifies the direction of the data flow. This determines the formats that the resulting enumerator can enumerate.


## -enum-fields




### -field DATADIR_GET

Requests that <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in<a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. 


### -field DATADIR_SET

Requests that <a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a> supply an enumerator for the formats that can be specified in <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a>. 



## -see-also




<a href="https://msdn.microsoft.com/657a7394-4481-4e0c-912d-40a9348caf16">IDataObject::EnumFormatEtc</a>



<a href="https://msdn.microsoft.com/6caebc68-a136-40f2-92d8-7f8003c18e5c">OleRegEnumFormatEtc</a>
 

 

