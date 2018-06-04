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

# IDiscMaster::EnumDiscMasterFormats


## -description


Retrieves an enumerator for all disc mastering formats supported by this disc master object. A disc master format specifies the structure of the content in a staged image file (data/audio) and the interface that manages the staged image.


## -parameters




### -param ppEnum [out]

Address of a pointer to the <b>IEnumDiscMasterFormats</b> enumerator.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



<b>MSDiscMasterObj</b> returns an enumerator that identifies the supported formats by their interface IDs. Currently, there are two formats: IID_IRedbookDiscMaster (
<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>) and IID_IJolietDiscMaster (
<a href="https://msdn.microsoft.com/e2269b68-1860-4afd-90f2-d61297f3fa9b">IJolietDiscMaster</a>).

<b>IEnumDiscMasterFormats</b> is standard COM enumerator, as documented in 
<b>IEnumXXXX</b>. Each call to <b>Next</b> returns an array of IIDs, one IID per supported disc master format. To select the active format and retrieve a pointer to a format specific interface, use 
<a href="https://msdn.microsoft.com/fcc2840b-d302-4cd6-b576-1826c83b711e">SetActiveDiscMasterFormat</a>. (Do not use <b>QueryInterface</b>, because the interface will not be associated with the active format).




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

