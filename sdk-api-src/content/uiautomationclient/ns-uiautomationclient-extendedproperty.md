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

# ExtendedProperty structure


## -description


Contains information about an extended property. 


## -struct-fields




### -field PropertyName

Type: <b>BSTR</b>

A localized string that contains the name of the extended property.


### -field PropertyValue

Type: <b>BSTR</b>

A string that represents the value of the extended property.   This string should be localized, if appropriate. 


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/D284E4B6-A328-4D79-A95F-DACE00042AF2">IUIAutomationStylesPattern::GetCachedExtendedPropertiesArray</a> and <a href="https://msdn.microsoft.com/AA128739-FB03-4E68-904B-648AE34A175C">GetCurrentExtendedPropertiesArray</a> methods.



