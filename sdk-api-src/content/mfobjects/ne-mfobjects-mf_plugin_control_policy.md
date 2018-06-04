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

# MF_PLUGIN_CONTROL_POLICY enumeration


## -description


Defines policy settings for the <a href="https://msdn.microsoft.com/1B078EB2-D87E-46A4-B2E1-A850C4E543A8">IMFPluginControl2::SetPolicy</a> method.


## -enum-fields




### -field MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS

Enumerate all registered sources and transforms.


### -field MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS

Enumerate only approved sources and transforms. Third-party components are excluded unless the component is registered with a valid merit value, or the component was registered locally by the application.


### -field MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS

Restrict enumeration to components intended for use in a web browser. 


### -field MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS_EDGEMODE




## -see-also




<a href="https://msdn.microsoft.com/15BD57FC-7CEF-45DC-AF94-3E54A3A9477A">IMFPluginControl2</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

