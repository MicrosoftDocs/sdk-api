---
UID: NN:vds.IVdsAdviseSink
title: IVdsAdviseSink (vds.h)
description: The IVdsAdviseSink interface (vds.h) receives VDS notifications.
helpviewer_keywords: ["IVdsAdviseSink","IVdsAdviseSink interface [VDS]","IVdsAdviseSink interface [VDS]","described","base.ivdsadvisesink","vds/IVdsAdviseSink","vdshwprv/IVdsAdviseSink"]
old-location: base\ivdsadvisesink.htm
tech.root: base
ms.assetid: 8e9b7c95-0b59-4268-a274-5d16812075a6
ms.date: 08/08/2022
ms.keywords: IVdsAdviseSink, IVdsAdviseSink interface [VDS], IVdsAdviseSink interface [VDS],described, base.ivdsadvisesink, vds/IVdsAdviseSink, vdshwprv/IVdsAdviseSink
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
 - IVdsAdviseSink
 - vds/IVdsAdviseSink
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
 - IVdsAdviseSink
---

# IVdsAdviseSink interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Receives VDS 
   notifications.

## -inheritance

The <b>IVdsAdviseSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAdviseSink</b> also has these types of members:

## -remarks

VDS registers an <b>IVdsAdviseSink</b> interface with 
    providers by calling the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">IVdsProviderPrivate::OnLoad</a> method 
    implemented by the provider.

After implementing the <b>IVdsAdviseSink</b> 
      interface, an application must register the interface with VDS to receive notifications. To register, call the 
      <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method and pass a pointer to the <b>IVdsAdviseSink</b> 
      interface. To unregister the <b>IVdsAdviseSink</b> interface and stop receiving notifications, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">IVdsService::Unadvise</a> method.<div class="alert"><b>Note</b>  An application that calls <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">Advise</a> must eventually call <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">Unadvise</a>. Ideally, it should call <b>Unadvise</b> as soon as it no longer needs to receive notifications.</div>
<div> </div>


You do not specify a notification type or an object type when you register an application for notifications. 
     Rather, you register to receive all VDS notifications of all types and from all providers.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">IVdsProviderPrivate::OnLoad</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="/windows/desktop/VDS/vds-notification-model">VDS Notifications</a>
