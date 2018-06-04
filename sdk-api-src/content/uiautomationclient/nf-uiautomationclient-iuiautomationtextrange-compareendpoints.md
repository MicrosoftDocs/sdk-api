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

# IUIAutomationTextRange::CompareEndpoints


## -description


Retrieves a value that specifies whether the start or end endpoint of this text range is the same as the start or end endpoint of another text range.


## -parameters




### -param srcEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of this text range is to be compared.


### -param range [in]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>*</b>

A pointer to the text range to compare.


### -param targetEndPoint [in]

Type: <b><a href="https://msdn.microsoft.com/4a294376-a401-4380-ba5a-b899548290b7">TextPatternRangeEndpoint</a></b>

A value indicating whether the start or end endpoint of <i>range</i> is to be compared.


### -param compValue [out, retval]

Type: <b>int*</b>

Receives a negative value if the caller's endpoint occurs earlier in the text than the target endpoint; 0 if the caller's endpoint is at the same location as the target endpoint; or a positive value if the caller's endpoint occurs later in the text than the target endpoint.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

