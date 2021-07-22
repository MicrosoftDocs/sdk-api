---
UID: NF:mfobjects.IMFPluginControl2.SetPolicy
title: IMFPluginControl2::SetPolicy (mfobjects.h)
description: Sets the policy for which media sources and transforms are enumerated.
helpviewer_keywords: ["IMFPluginControl2 interface [Media Foundation]","SetPolicy method","IMFPluginControl2.SetPolicy","IMFPluginControl2::SetPolicy","SetPolicy","SetPolicy method [Media Foundation]","SetPolicy method [Media Foundation]","IMFPluginControl2 interface","mf.imfplugincontrol2_setpolicy","mfobjects/IMFPluginControl2::SetPolicy"]
old-location: mf\imfplugincontrol2_setpolicy.htm
tech.root: mf
ms.assetid: 1B078EB2-D87E-46A4-B2E1-A850C4E543A8
ms.date: 12/05/2018
ms.keywords: IMFPluginControl2 interface [Media Foundation],SetPolicy method, IMFPluginControl2.SetPolicy, IMFPluginControl2::SetPolicy, SetPolicy, SetPolicy method [Media Foundation], SetPolicy method [Media Foundation],IMFPluginControl2 interface, mf.imfplugincontrol2_setpolicy, mfobjects/IMFPluginControl2::SetPolicy
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPluginControl2::SetPolicy
 - mfobjects/IMFPluginControl2::SetPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFPluginControl2.SetPolicy
---

# IMFPluginControl2::SetPolicy


## -description

Sets the policy for which media sources and transforms are enumerated.

## -parameters

### -param policy [in]

A value from the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy">MF_PLUGIN_CONTROL_POLICY</a> enumeration that specifies the policy.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2">IMFPluginControl2</a>