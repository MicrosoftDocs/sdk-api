---
UID: NF:vsbackup.IVssWMComponent.GetComponentInfo
title: IVssWMComponent::GetComponentInfo (vsbackup.h)
description: The GetComponentInfo method obtains basic information about the specified writer metadata component.
helpviewer_keywords: ["GetComponentInfo","GetComponentInfo method [VSS]","GetComponentInfo method [VSS]","IVssWMComponent interface","IVssWMComponent interface [VSS]","GetComponentInfo method","IVssWMComponent.GetComponentInfo","IVssWMComponent::GetComponentInfo","_win32_ivsswmcomponent_getcomponentinfo","base.ivsswmcomponent_getcomponentinfo","vsbackup/IVssWMComponent::GetComponentInfo"]
old-location: base\ivsswmcomponent_getcomponentinfo.htm
tech.root: base
ms.assetid: ac01bfea-e60f-4f50-a865-5bb7e372fbf2
ms.date: 12/05/2018
ms.keywords: GetComponentInfo, GetComponentInfo method [VSS], GetComponentInfo method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],GetComponentInfo method, IVssWMComponent.GetComponentInfo, IVssWMComponent::GetComponentInfo, _win32_ivsswmcomponent_getcomponentinfo, base.ivsswmcomponent_getcomponentinfo, vsbackup/IVssWMComponent::GetComponentInfo
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
 - IVssWMComponent::GetComponentInfo
 - vsbackup/IVssWMComponent::GetComponentInfo
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
 - IVssWMComponent.GetComponentInfo
---

# IVssWMComponent::GetComponentInfo


## -description

The 
<b>GetComponentInfo</b> method obtains basic information about the specified writer metadata component.

## -parameters

### -param ppInfo [out]

Doubly indirect pointer to a 
<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> structure containing the returned component information.

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
Successfully returned the component information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The caller is responsible for freeing the returned 
<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> structure by calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-freecomponentinfo">IVssWMComponent::FreeComponentInfo</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>



<a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a>