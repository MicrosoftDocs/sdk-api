---
UID: NL:vsbackup.IVssWMComponent
title: IVssWMComponent (vsbackup.h)
description: The IVssWMComponent is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.
helpviewer_keywords: ["IVssWMComponent","IVssWMComponent interface [VSS]","IVssWMComponent interface [VSS]","described","_win32_ivsswmcomponent","base.ivsswmcomponent","vsbackup/IVssWMComponent"]
old-location: base\ivsswmcomponent.htm
tech.root: base
ms.assetid: 8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95
ms.date: 12/05/2018
ms.keywords: IVssWMComponent, IVssWMComponent interface [VSS], IVssWMComponent interface [VSS],described, _win32_ivsswmcomponent, base.ivsswmcomponent, vsbackup/IVssWMComponent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssWMComponent
 - vsbackup/IVssWMComponent
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
 - IVssWMComponent
---

# IVssWMComponent class


## -description

The 
<b>IVssWMComponent</b> is a C++ (not COM) interface that allows access to component information stored in a Writer Metadata Document.

Instances of 
<b>IVssWMComponent</b> are obtained by calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a>.

## -inheritance

The <b>IVssWMComponent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssWMComponent</b> also has these types of members:

