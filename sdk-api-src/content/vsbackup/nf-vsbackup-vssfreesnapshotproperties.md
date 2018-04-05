---
UID: NF:vsbackup.VssFreeSnapshotProperties
title: VssFreeSnapshotProperties function
author: windows-driver-content
description: The VssFreeSnapshotProperties function is used to free the contents of a VSS_SNAPSHOT_PROP structure as part of managing its life cycle.
old-location: base\vssfreesnapshotproperties.htm
old-project: VSS
ms.assetid: d5b5883b-03d5-4a83-af2e-f4d22e26ee82
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: VssFreeSnapshotProperties, VssFreeSnapshotProperties function [VSS], VssFreeSnapshotPropertiesInternal, _win32_vssfreesnapshotproperties, base.vssfreesnapshotproperties, vsbackup/VssFreeSnapshotProperties, vsbackup/VssFreeSnapshotPropertiesInternal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VssApi.dll
-	Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
api_name:
-	VssFreeSnapshotProperties
-	VssFreeSnapshotPropertiesInternal
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
---

# VssFreeSnapshotProperties function


## -description


The <b>VssFreeSnapshotProperties</b> function is 
    used to free the contents of a <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> 
    structure as part of managing its life cycle. The 
    <b>VSS_SNAPSHOT_PROP</b> structure is typically obtained by 
    using the 
    <a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a> method or the <a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a> method.

This function can also be used to initialize a 
    <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure before use or before 
    freeing the structure.
<div class="alert"><b>Note</b>  This function is exported as <b>VssFreeSnapshotPropertiesInternal</b>, but you should call <b>VssFreeSnapshotProperties</b>, not <b>VssFreeSnapshotPropertiesInternal</b>.</div><div> </div>

## -parameters




### -param pProp [in]

Pointer to a valid <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> 
      object.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">IVssBackupComponents::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/59886344-d594-4eb8-9718-ab11a6627e8e">IVssSoftwareSnapshotProvider::GetSnapshotProperties</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>
 

 

