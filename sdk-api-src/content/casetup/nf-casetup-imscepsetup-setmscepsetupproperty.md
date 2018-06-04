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

# IMSCEPSetup::SetMSCEPSetupProperty


## -description


The <b>SetMSCEPSetupProperty</b> method sets a property value for a Network Device Enrollment Service (NDES) configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a> enumeration that specifies the type of property to configure.


### -param pPropertyValue [in]

A pointer to a  <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>
 

 

