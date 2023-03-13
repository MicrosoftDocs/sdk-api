---
UID: NN:vds.IVdsControllerControllerPort
title: IVdsControllerControllerPort (vds.h)
description: The IVdsControllerControllerPort interface (vds.h) provides a method to enumerate controller ports for a class implementing the IVdsController interface.
helpviewer_keywords: ["IVdsControllerControllerPort","IVdsControllerControllerPort interface [VDS]","IVdsControllerControllerPort interface [VDS]","described","base.ivdscontrollercontrollerport","vds/IVdsControllerControllerPort","vdshwprv/IVdsControllerControllerPort"]
old-location: base\ivdscontrollercontrollerport.htm
tech.root: base
ms.assetid: 15b09f97-c729-4687-a62c-dac57661f8c0
ms.date: 08/08/2022
ms.keywords: IVdsControllerControllerPort, IVdsControllerControllerPort interface [VDS], IVdsControllerControllerPort interface [VDS],described, base.ivdscontrollercontrollerport, vds/IVdsControllerControllerPort, vdshwprv/IVdsControllerControllerPort
req.header: vds.h
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
 - IVdsControllerControllerPort
 - vds/IVdsControllerControllerPort
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
 - IVdsControllerControllerPort
---

# IVdsControllerControllerPort interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to enumerate controller ports for a class implementing the 
   <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a> interface. This is needed to support 
   MPIO.

## -inheritance

The <b>IVdsControllerControllerPort</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsControllerControllerPort</b> also has these types of members:

## -see-also

<a href="/windows/desktop/VDS/controller-object">Controller Object</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollercontrollerport-querycontrollerports">QueryControllerPorts</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
