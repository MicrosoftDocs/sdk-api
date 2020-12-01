---
UID: NF:vsbackup.IVssWMComponent.FreeComponentInfo
title: IVssWMComponent::FreeComponentInfo (vsbackup.h)
description: The FreeComponentInfo method deallocates system resources devoted to the specified component information.
helpviewer_keywords: ["FreeComponentInfo","FreeComponentInfo method [VSS]","FreeComponentInfo method [VSS]","IVssWMComponent interface","IVssWMComponent interface [VSS]","FreeComponentInfo method","IVssWMComponent.FreeComponentInfo","IVssWMComponent::FreeComponentInfo","_win32_ivsswmcomponent_freecomponentinfo","base.ivsswmcomponent_freecomponentinfo","vsbackup/IVssWMComponent::FreeComponentInfo"]
old-location: base\ivsswmcomponent_freecomponentinfo.htm
tech.root: base
ms.assetid: 3f0c4634-2b1c-4a9b-9c13-ace38e03a7ce
ms.date: 12/05/2018
ms.keywords: FreeComponentInfo, FreeComponentInfo method [VSS], FreeComponentInfo method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],FreeComponentInfo method, IVssWMComponent.FreeComponentInfo, IVssWMComponent::FreeComponentInfo, _win32_ivsswmcomponent_freecomponentinfo, base.ivsswmcomponent_freecomponentinfo, vsbackup/IVssWMComponent::FreeComponentInfo
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssWMComponent::FreeComponentInfo
 - vsbackup/IVssWMComponent::FreeComponentInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWMComponent.FreeComponentInfo
---

# IVssWMComponent::FreeComponentInfo


## -description

The 
<b>FreeComponentInfo</b> method deallocates system resources devoted to the specified component information.

## -parameters

### -param pInfo [out]

Pointer to a 
<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> structure that contains the component information.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully freed the component information data.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>



<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a>