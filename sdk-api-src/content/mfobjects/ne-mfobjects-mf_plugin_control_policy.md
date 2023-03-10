---
UID: NE:mfobjects.MF_PLUGIN_CONTROL_POLICY
title: MF_PLUGIN_CONTROL_POLICY (mfobjects.h)
description: Defines policy settings for the IMFPluginControl2::SetPolicy method.
helpviewer_keywords: ["MF_PLUGIN_CONTROL_POLICY","MF_PLUGIN_CONTROL_POLICY enumeration [Media Foundation]","MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS","MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS","MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS","mf.mf_plugin_control_policy","mfobjects/MF_PLUGIN_CONTROL_POLICY","mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS","mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS","mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS"]
old-location: mf\mf_plugin_control_policy.htm
tech.root: mf
ms.assetid: AEA55D69-B3F1-463E-9DEC-B6BF7B9859D6
ms.date: 12/05/2018
ms.keywords: MF_PLUGIN_CONTROL_POLICY, MF_PLUGIN_CONTROL_POLICY enumeration [Media Foundation], MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS, MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS, MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS, mf.mf_plugin_control_policy, mfobjects/MF_PLUGIN_CONTROL_POLICY, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS, mfobjects/MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS
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
targetos: Windows
req.typenames: MF_PLUGIN_CONTROL_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MF_PLUGIN_CONTROL_POLICY
 - mfobjects/MF_PLUGIN_CONTROL_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_PLUGIN_CONTROL_POLICY
---

# MF_PLUGIN_CONTROL_POLICY enumeration


## -description

Defines policy settings for the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfplugincontrol2-setpolicy">IMFPluginControl2::SetPolicy</a> method.

## -enum-fields

### -field MF_PLUGIN_CONTROL_POLICY_USE_ALL_PLUGINS:0

Enumerate all registered sources and transforms.

### -field MF_PLUGIN_CONTROL_POLICY_USE_APPROVED_PLUGINS:1

Enumerate only approved sources and transforms. Third-party components are excluded unless the component is registered with a valid merit value, or the component was registered locally by the application.

### -field MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS:2

Restrict enumeration to components intended for use in a web browser.

### -field MF_PLUGIN_CONTROL_POLICY_USE_WEB_PLUGINS_EDGEMODE:3

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2">IMFPluginControl2</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
