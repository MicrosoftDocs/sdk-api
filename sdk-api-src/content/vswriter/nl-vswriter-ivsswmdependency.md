---
UID: NL:vswriter.IVssWMDependency
title: IVssWMDependency
author: windows-sdk-content
description: The IVssWMDependency is a C++ (not COM) interface returned by the IVssWMComponent interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer.
old-location: base\ivsswmdependency.htm
tech.root: VSS
ms.assetid: 5ec3d8d2-5138-4887-9741-addaaaee6bee
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVssWMDependency, IVssWMDependency interface [VSS], IVssWMDependency interface [VSS],described, _win32_ivsswmdependency, base.ivsswmdependency, vswriter/IVssWMDependency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssWMDependency class


## -description


The 
<b>IVssWMDependency</b> is a C++ (not COM) interface returned by the 
<a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a> interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer. (Dependencies must be between writers, not within writers.)

<b>IVssWMDependency</b> is used to determine the writer ID, logical path, and component name of components that must be restored or backed up along with the target component.

Dependencies are created by writers while handling <a href="https://msdn.microsoft.com/en-us/library/Aa384659(v=VS.85).aspx">Identify</a> events (<a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriter::OnIdentify</a>) using the 
<a href="https://msdn.microsoft.com/cc6c8ab6-3706-4c75-ba31-cc8c1dc4dd06">IVssCreateWriterMetadata::AddComponentDependency</a> method.

Calling applications are responsible for calling <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> to release resources held by a returned 
<b>IVssWMDependency</b> object when it is no longer needed.

The 
<a href="https://msdn.microsoft.com/ead9ff63-15dc-4fcc-b341-85ad9c3eabb7">IVssWMComponent::GetDependency</a> method returns an 
<b>IVssWMDependency</b> interface.

Note that a dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on. A dependency merely indicates that the component and the components it depends on must always be backed up or restored together.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssWMDependency</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssWMDependency</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b0115a42-3c74-41a0-8062-0f20123780fe">GetComponentName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a component that the current component depends on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/642e9266-40b8-4184-b83f-3131886da32b">GetLogicalPath</a>
</td>
<td align="left" width="63%">
Retrieves the logical path of a component that the current component depends on.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/275843c5-3a8c-4add-b453-53ff5d2bb868">GetWriterId</a>
</td>
<td align="left" width="63%">
Retrieves the class ID of a writer containing a component that the current component depends on.

</td>
</tr>
</table> 

