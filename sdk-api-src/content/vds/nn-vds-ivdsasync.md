---
UID: NN:vds.IVdsAsync
title: IVdsAsync (vds.h)
description: The IVdsAsync interface (vds.h) manages asynchronous operations.
helpviewer_keywords: ["IVdsAsync","IVdsAsync interface [VDS]","IVdsAsync interface [VDS]","described","base.ivdsasync","vds/IVdsAsync","vdshwprv/IVdsAsync"]
old-location: base\ivdsasync.htm
tech.root: base
ms.assetid: 7814b8ef-84b4-453e-b480-c32b67e5af93
ms.date: 08/08/2022
ms.keywords: IVdsAsync, IVdsAsync interface [VDS], IVdsAsync interface [VDS],described, base.ivdsasync, vds/IVdsAsync, vdshwprv/IVdsAsync
req.header: vds.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAsync
 - vds/IVdsAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAsync
---

# IVdsAsync interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Manages asynchronous 
   operations. Methods that initiate asynchronous operations return a pointer to an 
   <b>IVdsAsync</b> interface, allowing the caller to optionally 
   cancel, wait for, or query the status of the asynchronous operation.

## -inheritance

The <b>IVdsAsync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAsync</b> also has these types of members:

## -see-also

<a href="/windows/desktop/VDS/helper-objects">Helper Objects</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-next">IEnumVdsObject::Next</a>



<a href="/windows/desktop/VDS/managing-asynchronous-operations">Managing Asynchronous Operations</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
