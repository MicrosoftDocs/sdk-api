---
UID: NN:vdshwprv.IVdsHwProviderPrivateMpio
title: IVdsHwProviderPrivateMpio (vdshwprv.h)
description: Provides a method that sets the status of paths originating from a particular HBA port to the provider.
helpviewer_keywords: ["IVdsHwProviderPrivateMpio","IVdsHwProviderPrivateMpio interface [VDS]","IVdsHwProviderPrivateMpio interface [VDS]","described","base.ivdshwproviderprivatempio","vdshwprv/IVdsHwProviderPrivateMpio"]
old-location: base\ivdshwproviderprivatempio.htm
tech.root: base
ms.assetid: fa60e832-1148-4ffb-bf70-bd7b27180cdd
ms.date: 12/05/2018
ms.keywords: IVdsHwProviderPrivateMpio, IVdsHwProviderPrivateMpio interface [VDS], IVdsHwProviderPrivateMpio interface [VDS],described, base.ivdshwproviderprivatempio, vdshwprv/IVdsHwProviderPrivateMpio
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
 - IVdsHwProviderPrivateMpio
 - vdshwprv/IVdsHwProviderPrivateMpio
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
 - IVdsHwProviderPrivateMpio
---

# IVdsHwProviderPrivateMpio interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method that sets the status of paths originating from a particular HBA port to the provider.

## -inheritance

The <b>IVdsHwProviderPrivateMpio</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsHwProviderPrivateMpio</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderprivatempio-setallpathstatusesfromhbaport">SetAllPathStatusesFromHbaPort</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
