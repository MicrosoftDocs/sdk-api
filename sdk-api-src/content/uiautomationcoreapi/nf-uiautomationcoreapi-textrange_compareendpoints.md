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

# TextRange_CompareEndpoints function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns a value indicating whether two text ranges have identical endpoints.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The starting or ending endpoint of <i>hobj</i>.


### -param targetRange [in]

Type: <b>ITextRangeInteropProvider*</b>

The text range that is being compared against.


### -param targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The starting or ending endpoint of <i>targetRange</i>.


### -param pRetVal [out]

Type: <b>int*</b>

The address of a variable that receives a pointer to a value that indicates whether two text ranges have identical endpoints.
				 This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks




			The returned value is &lt;0 if the caller's endpoint occurs earlier in the text than the target endpoint; 
			0 if the caller's endpoint is at the same location as the target endpoint; and 
			&gt;0 if the caller's endpoint occurs later in the text than the target endpoint.
			



