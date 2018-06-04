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

# UiaLookupId function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.


## -parameters




### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/798afc92-73bc-4a76-a8bb-afa804038205">AutomationIdentifierType</a></b>

A value from the <a href="https://msdn.microsoft.com/798afc92-73bc-4a76-a8bb-afa804038205">AutomationIdentifierType</a> enumerated type that specifies the type of identifier to look up.


### -param pGuid [in]

Type: <b>GUID*</b>

The address of the unique identifier of the property, pattern, control type, text attribute, or event.


## -returns



Type: <b>int</b>

Returns an integer identifier.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b8e9e33c-9781-4f50-bbb7-a9950409f2e6">GUIDs</a>



<a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>
 

 

