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

# TextRange_ExpandToEnclosingUnit function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/518318fc-d60f-41b7-a6da-1f2bf5c2e494">TextUnit</a></b>

The unit that the provider must expand the text range to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



If the range is already an integral number of the specified units, it remains unchanged.

If the starting endpoint is not at a <a href="https://msdn.microsoft.com/518318fc-d60f-41b7-a6da-1f2bf5c2e494">TextUnit</a> boundary, it is moved backward until it is at a boundary. 
			Subsequently, if the ending endpoint is not at a boundary, or if it is at the same boundary as the starting endpoint, 
			the ending endpoint is moved forward until it is at a boundary.

<div class="alert"><b>Note</b>  It is common for a screen reader to read out a full word, entire paragraph, and so on, 
			at the insertion point or any virtual cursor position.
</div>
<div> </div>
<b>TextRange_ExpandToEnclosingUnit</b> respects both hidden and visible text. The UI Automation
			client can check the is-hidden attribute (Text_IsHidden_Attribute_GUID) for text visibility.

<b>TextRange_ExpandToEnclosingUnit</b> defaults up to the next supported <a href="https://msdn.microsoft.com/518318fc-d60f-41b7-a6da-1f2bf5c2e494">TextUnit</a> if the given <b>TextUnit</b> is not supported by the control.



