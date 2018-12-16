---
UID: NE:mfobjects.MF_PLUGIN_CONTROL_POLICY
title: MF_PLUGIN_CONTROL_POLICY
author: windows-sdk-content
description: Defines policy settings for the IMFPluginControl2::SetPolicy method.
old-location: mf\mf_plugin_control_policy.htm
tech.root: medfound
ms.assetid: AEA55D69-B3F1-463E-9DEC-B6BF7B9859D6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MF_PLUGIN_CONTROL_POLICY, MF_PLUGIN_CONTROL_POLICY enumeration [Media Foundation], MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS, MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS, MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS, mf.mf_plugin_control_policy, mfobjects/MF_PLUGIN_CONTROL_POLICY, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_PLUGIN_CONTROL_POLICY
product: Windows
targetos: Windows
req.typenames: MF_PLUGIN_CONTROL_POLICY
req.redist: 
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
 

 

