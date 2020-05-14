---
UID: NF:vswriter.CVssWriter.IsPartialFileSupportEnabled
title: CVssWriter::IsPartialFileSupportEnabled (vswriter.h)
description: The IsPartialFileSupportEnabled method determines whether partial file support is enabled or disabled.helpviewer_keywords: ["CVssWriter class [VSS]","IsPartialFileSupportEnabled method","CVssWriter.IsPartialFileSupportEnabled","CVssWriter::IsPartialFileSupportEnabled","IsPartialFileSupportEnabled","IsPartialFileSupportEnabled method [VSS]","IsPartialFileSupportEnabled method [VSS]","CVssWriter class","_win32_cvsswriter_ispartialfilesupportenabled","base.cvsswriter_ispartialfilesupportenabled","vswriter/CVssWriter::IsPartialFileSupportEnabled"]
old-location: base\cvsswriter_ispartialfilesupportenabled.htm
tech.root: VSS
ms.assetid: f0552573-6b67-412d-aad0-d182ee50923f
ms.date: 12/05/2018
ms.keywords: CVssWriter class [VSS],IsPartialFileSupportEnabled method, CVssWriter.IsPartialFileSupportEnabled, CVssWriter::IsPartialFileSupportEnabled, IsPartialFileSupportEnabled, IsPartialFileSupportEnabled method [VSS], IsPartialFileSupportEnabled method [VSS],CVssWriter class, _win32_cvsswriter_ispartialfilesupportenabled, base.cvsswriter_ispartialfilesupportenabled, vswriter/CVssWriter::IsPartialFileSupportEnabled
f1_keywords:
- vswriter/CVssWriter.IsPartialFileSupportEnabled
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- CVssWriter.IsPartialFileSupportEnabled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriter::IsPartialFileSupportEnabled


## -description


The 
<b>IsPartialFileSupportEnabled</b> method determines whether partial file support is enabled or disabled.

<b>IsPartialFileSupportEnabled</b> is a protected method implemented by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.


## -parameters






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
<dt><b>true</b></dt>
</dl>
</td>
<td width="60%">
The requester supports partial file backups and restores.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>false</b></dt>
</dl>
</td>
<td width="60%">
The requester supports only the backup and restore of entire files.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>
 

 

