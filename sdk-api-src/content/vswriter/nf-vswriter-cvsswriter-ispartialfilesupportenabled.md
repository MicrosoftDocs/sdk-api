---
UID: NF:vswriter.CVssWriter.IsPartialFileSupportEnabled
title: CVssWriter::IsPartialFileSupportEnabled
author: windows-sdk-content
description: The IsPartialFileSupportEnabled method determines whether partial file support is enabled or disabled.
old-location: base\cvsswriter_ispartialfilesupportenabled.htm
old-project: vss
ms.assetid: f0552573-6b67-412d-aad0-d182ee50923f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CVssWriter class [VSS],IsPartialFileSupportEnabled method, CVssWriter.IsPartialFileSupportEnabled, CVssWriter::IsPartialFileSupportEnabled, IsPartialFileSupportEnabled, IsPartialFileSupportEnabled method [VSS], IsPartialFileSupportEnabled method [VSS],CVssWriter class, _win32_cvsswriter_ispartialfilesupportenabled, base.cvsswriter_ispartialfilesupportenabled, vswriter/CVssWriter::IsPartialFileSupportEnabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::IsPartialFileSupportEnabled


## -description


The 
<b>IsPartialFileSupportEnabled</b> method determines whether partial file support is enabled or disabled.

<b>IsPartialFileSupportEnabled</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


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




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>
 

 

