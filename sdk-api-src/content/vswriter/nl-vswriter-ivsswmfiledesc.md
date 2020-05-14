---
UID: NL:vswriter.IVssWMFiledesc
title: IVssWMFiledesc (vswriter.h)
description: The IVssWMFiledesc interface is a C++ (not COM) interface returned to a calling application by a number of query methods. It provides detailed information about a file or set of files (a file set).helpviewer_keywords: ["IVssWMFiledesc","IVssWMFiledesc interface [VSS]","IVssWMFiledesc interface [VSS]","described","_win32_ivsswmfiledesc","base.ivsswmfiledesc","vswriter/IVssWMFiledesc"]
old-location: base\ivsswmfiledesc.htm
tech.root: VSS
ms.assetid: 0b86882d-af1b-4a09-8c25-5b806c9ca909
ms.date: 12/05/2018
ms.keywords: IVssWMFiledesc, IVssWMFiledesc interface [VSS], IVssWMFiledesc interface [VSS],described, _win32_ivsswmfiledesc, base.ivsswmfiledesc, vswriter/IVssWMFiledesc
f1_keywords:
- vswriter/IVssWMFiledesc
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
- IVssWMFiledesc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssWMFiledesc class


## -description


The 
<b>IVssWMFiledesc</b> interface is a C++ (not COM) interface returned to a calling application by a number of query methods. It provides detailed information about a file or set of files (a file set).

The calling application is responsible for calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the resources held by the returned 
<b>IVssWMFiledesc</b> interface when it is no longer needed.

The following methods return an 
<b>IVssWMFiledesc</b> interface:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">IVssComponent::GetAlternateLocationMapping</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtarget">IVssComponent::GetNewTarget</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile">IVssExamineWriterMetadata::GetExcludeFile</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getfile">IVssWMComponent::GetFile</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabasefile">IVssWMComponent::GetDatabaseFile</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">IVssWMComponent::GetDatabaseLogFile</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMFiledesc</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssWMFiledesc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssWMFiledesc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getalternatelocation">GetAlternateLocation</a>
</td>
<td align="left" width="63%">
Obtains the alternate backup location of the component files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask">GetBackupTypeMask</a>
</td>
<td align="left" width="63%">
Obtains the file backup specification for a file or set of files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getfilespec">GetFilespec</a>
</td>
<td align="left" width="63%">
Obtains the file specification for the list of files provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Obtains the fully qualified directory path for the list of files provided.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getrecursive">GetRecursive</a>
</td>
<td align="left" width="63%">
Determines whether only files in the root directory or files in the entire directory hierarchy are considered for backup.

</td>
</tr>
</table> 

