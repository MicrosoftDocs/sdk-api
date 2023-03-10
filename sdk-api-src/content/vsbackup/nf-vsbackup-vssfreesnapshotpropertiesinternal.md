---
UID: NF:vsbackup.VssFreeSnapshotPropertiesInternal
title: VssFreeSnapshotPropertiesInternal function (vsbackup.h)
description: The VssFreeSnapshotPropertiesInternal function (vsbackup.h) is used to free the contents of a VSS_SNAPSHOT_PROP structure as part of managing its life cycle.
helpviewer_keywords: ["VssFreeSnapshotProperties","VssFreeSnapshotProperties function [VSS]","VssFreeSnapshotPropertiesInternal","_win32_vssfreesnapshotproperties","base.vssfreesnapshotproperties","vsbackup/VssFreeSnapshotProperties","vsbackup/VssFreeSnapshotPropertiesInternal"]
old-location: base\vssfreesnapshotproperties.htm
tech.root: base
ms.assetid: d5b5883b-03d5-4a83-af2e-f4d22e26ee82
ms.date: 08/09/2022
ms.keywords: VssFreeSnapshotProperties, VssFreeSnapshotProperties function [VSS], VssFreeSnapshotPropertiesInternal, _win32_vssfreesnapshotproperties, base.vssfreesnapshotproperties, vsbackup/VssFreeSnapshotProperties, vsbackup/VssFreeSnapshotPropertiesInternal
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
req.dll: VssApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VssFreeSnapshotPropertiesInternal
 - vsbackup/VssFreeSnapshotPropertiesInternal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VssApi.dll
 - Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
api_name:
 - VssFreeSnapshotProperties
 - VssFreeSnapshotPropertiesInternal
---

# VssFreeSnapshotPropertiesInternal function


## -description

The <b>VssFreeSnapshotProperties</b> function is 
    used to free the contents of a <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> 
    structure as part of managing its life cycle. The 
    <b>VSS_SNAPSHOT_PROP</b> structure is typically obtained by 
    using the 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a> method or the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-getsnapshotproperties">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a> method.

This function can also be used to initialize a 
    <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure before use or before 
    freeing the structure.
<div class="alert"><b>Note</b>  This function is exported as <b>VssFreeSnapshotPropertiesInternal</b>, but you should call <b>VssFreeSnapshotProperties</b>, not <b>VssFreeSnapshotPropertiesInternal</b>.</div><div> </div>

## -parameters

### -param pProp [in]

Pointer to a valid <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> 
      object.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">IVssBackupComponents::GetSnapshotProperties</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-getsnapshotproperties">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a>



<a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a>
