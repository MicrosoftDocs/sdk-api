---
UID: NN:vds.IVdsController
title: IVdsController (vds.h)
description: The IVdsController interface (vds.h) provides methods for performing query and configuration operations on a controller.
helpviewer_keywords: ["IVdsController","IVdsController interface [VDS]","IVdsController interface [VDS]","described","base.ivdscontroller","vds/IVdsController","vdshwprv/IVdsController"]
old-location: base\ivdscontroller.htm
tech.root: base
ms.assetid: cc30a78a-78a4-49c2-a97d-228400da46a9
ms.date: 08/08/2022
ms.keywords: IVdsController, IVdsController interface [VDS], IVdsController interface [VDS],described, base.ivdscontroller, vds/IVdsController, vdshwprv/IVdsController
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
 - IVdsController
 - vds/IVdsController
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
 - IVdsController
---

# IVdsController interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for 
   performing query and configuration operations on a controller.

## -inheritance

The <b>IVdsController</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsController</b> also has these types of members:

## -see-also

<a href="/windows/desktop/VDS/controller-object">Controller Object</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollercontrollerport">IVdsControllerControllerPort</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querycontrollers">IVdsSubSystem::QueryControllers</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_controller_prop">VDS_CONTROLLER_PROP</a>
