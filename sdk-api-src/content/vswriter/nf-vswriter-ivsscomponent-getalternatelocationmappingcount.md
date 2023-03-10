---
UID: NF:vswriter.IVssComponent.GetAlternateLocationMappingCount
title: IVssComponent::GetAlternateLocationMappingCount (vswriter.h)
description: The GetAlternateLocationMappingCount method returns the number of alternate location mappings used by a requester in restoring data. Either a writer or a requester can call this method.
helpviewer_keywords: ["GetAlternateLocationMappingCount","GetAlternateLocationMappingCount method [VSS]","GetAlternateLocationMappingCount method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetAlternateLocationMappingCount method","IVssComponent.GetAlternateLocationMappingCount","IVssComponent::GetAlternateLocationMappingCount","_win32_ivsscomponent_getalternatelocationmappingcount","base.ivsscomponent_getalternatelocationmappingcount","vswriter/IVssComponent::GetAlternateLocationMappingCount"]
old-location: base\ivsscomponent_getalternatelocationmappingcount.htm
tech.root: base
ms.assetid: 218dc021-0a9e-4ba7-95b7-e1f31e57e71c
ms.date: 12/05/2018
ms.keywords: GetAlternateLocationMappingCount, GetAlternateLocationMappingCount method [VSS], GetAlternateLocationMappingCount method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetAlternateLocationMappingCount method, IVssComponent.GetAlternateLocationMappingCount, IVssComponent::GetAlternateLocationMappingCount, _win32_ivsscomponent_getalternatelocationmappingcount, base.ivsscomponent_getalternatelocationmappingcount, vswriter/IVssComponent::GetAlternateLocationMappingCount
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssComponent::GetAlternateLocationMappingCount
 - vswriter/IVssComponent::GetAlternateLocationMappingCount
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
 - IVssComponent.GetAlternateLocationMappingCount
---

# IVssComponent::GetAlternateLocationMappingCount


## -description

The 
<b>GetAlternateLocationMappingCount</b> method returns the number of alternate location mappings used by a requester in restoring data. Either a writer or a requester can call this method.

## -parameters

### -param pcMappings [out]

The address of a caller-allocated variable that receives the number of alternate location mappings.

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
Successfully returned the attribute value.

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
</table>

## -remarks

The count of alternate location mappings returned by 
<b>GetAlternateLocationMappingCount</b> may be due to not only files in the current component but to files in any of its nonselectable subcomponents.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

The count returned by 
<b>GetAlternateLocationMappingCount</b> refers to the number of alternate location mappings used in the course of restoring files.

The count is updated by calls to 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping">IVssBackupComponents::AddAlternativeLocationMapping</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">IVssComponent::GetAlternateLocationMapping</a>