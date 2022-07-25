---
UID: NF:vswriter.CVssWriter.GetSnapshotDeviceName
title: CVssWriter::GetSnapshotDeviceName (vswriter.h)
description: The GetSnapshotDeviceName method returns the name of the device that hosts the shadow copy of the specified volume or file share.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetSnapshotDeviceName method","CVssWriter.GetSnapshotDeviceName","CVssWriter::GetSnapshotDeviceName","GetSnapshotDeviceName","GetSnapshotDeviceName method [VSS]","GetSnapshotDeviceName method [VSS]","CVssWriter interface","_win32_cvsswriter_getsnapshotdevicename","base.cvsswriter_getsnapshotdevicename","vswriter/CVssWriter::GetSnapshotDeviceName"]
old-location: base\cvsswriter_getsnapshotdevicename.htm
tech.root: base
ms.assetid: ac0beefe-0afd-45da-b1bb-1bd960b4b0f0
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetSnapshotDeviceName method, CVssWriter.GetSnapshotDeviceName, CVssWriter::GetSnapshotDeviceName, GetSnapshotDeviceName, GetSnapshotDeviceName method [VSS], GetSnapshotDeviceName method [VSS],CVssWriter interface, _win32_cvsswriter_getsnapshotdevicename, base.cvsswriter_getsnapshotdevicename, vswriter/CVssWriter::GetSnapshotDeviceName
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - CVssWriter::GetSnapshotDeviceName
 - vswriter/CVssWriter::GetSnapshotDeviceName
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
 - CVssWriter.GetSnapshotDeviceName
---

# CVssWriter::GetSnapshotDeviceName


## -description

The <b>GetSnapshotDeviceName</b> method 
   returns the name of the device that hosts the shadow copy of the specified volume or file share. This method allows writers to support 
   <a href="/windows/desktop/VSS/vssgloss-a">auto-recover</a> shadow copies, and 
   can only be called during the processing of the 
   <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">OnPostSnapshot</a> method.

## -parameters

### -param wszOriginalVolume [in]

Name of the original volume or the UNC path of the original file share that contains data used for the current shadow copy set. The name of the volume must be in one 
      of the following formats and must include a trailing backslash (\\):
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, 
        D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
<li>A UNC path that specifies a remote file share, for example, \\Clusterx\Share1\</li>
</ul>

### -param ppwszSnapshotDevice [out]

The address of a <b>LPCWSTR</b> that will receive a pointer to the device name of the 
      shadow copy.

## -returns

This method can return one of these values.

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
Successfully returned the shadow copy volume name.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The call was not made during the 
        <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot event</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>wszOriginalVolume</i> parameter is not one of the volumes or file shares in the shadow copy 
        set.

</td>
</tr>
</table>

## -remarks

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

To get the name of the original volume for the <i>wszOriginalVolume</i> parameter, first call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumecount">CVssWriter::GetCurrentVolumeCount</a> method to query the number of volumes in the shadow copy set. Then call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumearray">CVssWriter::GetCurrentVolumeArray</a> method to enumerate the original names of the volumes in the shadow copy set.