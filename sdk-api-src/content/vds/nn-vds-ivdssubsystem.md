---
UID: NN:vds.IVdsSubSystem
title: IVdsSubSystem (vds.h)
description: The IVdsSubSystem interface (vds.h) provides methods for performing query and configuration operations on a subsystem.  
helpviewer_keywords: ["IVdsSubSystem","IVdsSubSystem interface [VDS]","IVdsSubSystem interface [VDS]","described","base.ivdssubsystem","vds/IVdsSubSystem","vdshwprv/IVdsSubSystem"]
old-location: base\ivdssubsystem.htm
tech.root: base
ms.assetid: 1f1b9735-216b-4bc5-a9b8-2d274827b2c8
ms.date: 08/05/2022
ms.keywords: IVdsSubSystem, IVdsSubSystem interface [VDS], IVdsSubSystem interface [VDS],described, base.ivdssubsystem, vds/IVdsSubSystem, vdshwprv/IVdsSubSystem
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
 - IVdsSubSystem
 - vds/IVdsSubSystem
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
 - IVdsSubSystem
---

# IVdsSubSystem interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a subsystem.

## -inheritance

The <b>IVdsSubSystem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSubSystem</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getsubsystem">IVdsController::GetSubSystem</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getsubsystem">IVdsDrive::GetSubSystem</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-querysubsystems">IVdsHwProvider::QuerySubSystems</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getsubsystem">IVdsLun::GetSubSystem</a>



<a href="/windows/desktop/VDS/subsystem-object">Subsystem Object</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
