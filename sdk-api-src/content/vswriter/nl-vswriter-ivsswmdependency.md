---
UID: NL:vswriter.IVssWMDependency
title: IVssWMDependency (vswriter.h)
description: The IVssWMDependency is a C++ (not COM) interface returned by the IVssWMComponent interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer.
helpviewer_keywords: ["IVssWMDependency","IVssWMDependency interface [VSS]","IVssWMDependency interface [VSS]","described","_win32_ivsswmdependency","base.ivsswmdependency","vswriter/IVssWMDependency"]
old-location: base\ivsswmdependency.htm
tech.root: base
ms.assetid: 5ec3d8d2-5138-4887-9741-addaaaee6bee
ms.date: 12/05/2018
ms.keywords: IVssWMDependency, IVssWMDependency interface [VSS], IVssWMDependency interface [VSS],described, _win32_ivsswmdependency, base.ivsswmdependency, vswriter/IVssWMDependency
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssWMDependency
 - vswriter/IVssWMDependency
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
 - IVssWMDependency
---

# IVssWMDependency class


## -description

The 
<b>IVssWMDependency</b> is a C++ (not COM) interface returned by the 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> interface and used by applications when backing up or restoring a component that has an explicit writer-component dependency on a component managed by another writer. (Dependencies must be between writers, not within writers.)

<b>IVssWMDependency</b> is used to determine the writer ID, logical path, and component name of components that must be restored or backed up along with the target component.

Dependencies are created by writers while handling <a href="/windows/desktop/VSS/vssgloss-i">Identify</a> events (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a>) using the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency">IVssCreateWriterMetadata::AddComponentDependency</a> method.

Calling applications are responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release resources held by a returned 
<b>IVssWMDependency</b> object when it is no longer needed.

The 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdependency">IVssWMComponent::GetDependency</a> method returns an 
<b>IVssWMDependency</b> interface.

Note that a dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on. A dependency merely indicates that the component and the components it depends on must always be backed up or restored together.

## -inheritance

The <b>IVssWMDependency</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssWMDependency</b> also has these types of members:

