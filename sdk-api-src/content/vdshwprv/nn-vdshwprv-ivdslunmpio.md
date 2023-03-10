---
UID: NN:vdshwprv.IVdsLunMpio
title: IVdsLunMpio (vdshwprv.h)
description: The IVdsLunMpio interface (vdshwprv.h) provides methods for performing query and configuration operations on a LUN with MPIO extensions. 
helpviewer_keywords: ["IVdsLunMpio","IVdsLunMpio interface [VDS]","IVdsLunMpio interface [VDS]","described","base.ivdslunmpio","vds/IVdsLunMpio","vdshwprv/IVdsLunMpio"]
old-location: base\ivdslunmpio.htm
tech.root: base
ms.assetid: 0c7ab50a-306e-44f8-976d-0e65e36b0fea
ms.date: 08/08/2022
ms.keywords: IVdsLunMpio, IVdsLunMpio interface [VDS], IVdsLunMpio interface [VDS],described, base.ivdslunmpio, vds/IVdsLunMpio, vdshwprv/IVdsLunMpio
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsLunMpio
 - vdshwprv/IVdsLunMpio
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
 - IVdsLunMpio
---

# IVdsLunMpio interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a LUN with MPIO extensions.

## -inheritance

The <b>IVdsLunMpio</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunMpio</b> also has these types of members:

## -remarks

If your provider is an iSCSI provider, or if your provider does not support MPIO, you should not implement the <b>IVdsLunMpio</b> interface. If an iSCSI provider implements this interface, VDS will ignore it, because VDS uses the service's own routines to handle MPIO for iSCSI.

## -see-also

<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
