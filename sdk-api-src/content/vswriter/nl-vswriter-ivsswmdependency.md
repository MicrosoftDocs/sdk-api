---
UID: NL:vswriter.IVssWMDependency
title: IVssWMDependency (vswriter.h)
author: windows-sdk-content
description: The IVssWMDependency is a C++ (not COM) interface returned by the IVssWMComponent interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer.
old-location: base\ivsswmdependency.htm
tech.root: VSS
ms.assetid: 5ec3d8d2-5138-4887-9741-addaaaee6bee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssWMDependency, IVssWMDependency interface [VSS], IVssWMDependency interface [VSS],described, _win32_ivsswmdependency, base.ivsswmdependency, vswriter/IVssWMDependency
ms.topic: class
f1_keywords: 
 - "vswriter/IVssWMDependency"
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVssWMDependency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssWMDependency class


## -description


The 
<b>IVssWMDependency</b> is a C++ (not COM) interface returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer. (Dependencies must be between writers, not within writers.)

<b>IVssWMDependency</b> is used to determine the writer ID, logical path, and component name of components that must be restored or backed up along with the target component.

Dependencies are created by writers while handling <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-i">Identify</a> events (<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a>) using the 
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency">IVssCreateWriterMetadata::AddComponentDependency</a> method.

Calling applications are responsible for calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release resources held by a returned 
<b>IVssWMDependency</b> object when it is no longer needed.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdependency">IVssWMComponent::GetDependency</a> method returns an 
<b>IVssWMDependency</b> interface.

Note that a dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on. A dependency merely indicates that the component and the components it depends on must always be backed up or restored together.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMDependency</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssWMDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssWMDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmdependency-getcomponentname">GetComponentName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a component that the current component depends on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmdependency-getlogicalpath">GetLogicalPath</a>
</td>
<td align="left" width="63%">
Retrieves the logical path of a component that the current component depends on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswmdependency-getwriterid">GetWriterId</a>
</td>
<td align="left" width="63%">
Retrieves the class ID of a writer containing a component that the current component depends on.

</td>
</tr>
</table> 

