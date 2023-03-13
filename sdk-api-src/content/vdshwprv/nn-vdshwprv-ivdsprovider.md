---
UID: NN:vdshwprv.IVdsProvider
title: IVdsProvider (vdshwprv.h)
description: The IVdsProvider interface (vdshwprv.h) returns the properties of a hardware or software provider. 
helpviewer_keywords: ["IVdsProvider","IVdsProvider interface [VDS]","IVdsProvider interface [VDS]","described","base.ivdsprovider","vds/IVdsProvider","vdshwprv/IVdsProvider"]
old-location: base\ivdsprovider.htm
tech.root: base
ms.assetid: c09aa32f-d859-44b1-8656-973ba1b6a167
ms.date: 08/08/2022
ms.keywords: IVdsProvider, IVdsProvider interface [VDS], IVdsProvider interface [VDS],described, base.ivdsprovider, vds/IVdsProvider, vdshwprv/IVdsProvider
req.header: vdshwprv.h
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
 - IVdsProvider
 - vdshwprv/IVdsProvider
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
 - IVdsProvider
---

# IVdsProvider interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of 
   a hardware or software provider.

## -inheritance

The <b>IVdsProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdspack-getprovider">IVdsPack::GetProvider</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getprovider">IVdsSubSystem::GetProvider</a>



<a href="/windows/desktop/VDS/provider-object">Provider Object</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a>
