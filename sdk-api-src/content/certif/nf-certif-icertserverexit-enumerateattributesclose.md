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

# ICertServerExit::EnumerateAttributesClose


## -description


The <b>EnumerateAttributesClose</b> method frees any resources connected with <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> enumeration.

All applications that use 
<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a> or 
<a href="https://msdn.microsoft.com/df778207-3b20-45a5-a705-8dba566eb658">ICertServerExit::EnumerateAttributes</a> should call <b>EnumerateAttributesClose</b> when finished enumerating.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/df778207-3b20-45a5-a705-8dba566eb658">ICertServerExit::EnumerateAttributes</a>



<a href="https://msdn.microsoft.com/c81b9c4d-483e-48b8-a270-f570e148d371">ICertServerExit::EnumerateAttributesSetup</a>
 

 

