---
UID: NL:vsbackup.IVssWMComponent
title: IVssWMComponent (vsbackup.h)
description: The IVssWMComponent is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.
old-location: base\ivsswmcomponent.htm
tech.root: VSS
ms.assetid: 8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95
ms.date: 12/05/2018
ms.keywords: IVssWMComponent, IVssWMComponent interface [VSS], IVssWMComponent interface [VSS],described, _win32_ivsswmcomponent, base.ivsswmcomponent, vsbackup/IVssWMComponent
f1_keywords:
- vsbackup/IVssWMComponent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssWMComponent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssWMComponent class


## -description


The 
<b>IVssWMComponent</b> is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.

Instances of 
<b>IVssWMComponent</b> are obtained by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMComponent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssWMComponent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssWMComponent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-freecomponentinfo">FreeComponentInfo</a>
</td>
<td align="left" width="63%">
Deallocates system resources devoted to the specified component information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getcomponentinfo">GetComponentInfo</a>
</td>
<td align="left" width="63%">
Obtains basic information about the specified backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabasefile">GetDatabaseFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing information about the specified database backup component file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">GetDatabaseLogFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing information for the log file of a specified database backup component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdependency">GetDependency</a>
</td>
<td align="left" width="63%">
Returns the dependency information for a component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getfile">GetFile</a>
</td>
<td align="left" width="63%">
Obtains an 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object containing information about the specified member of a file group.

</td>
</tr>
</table> 

