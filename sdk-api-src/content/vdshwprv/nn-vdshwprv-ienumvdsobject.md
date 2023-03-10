---
UID: NN:vdshwprv.IEnumVdsObject
title: IEnumVdsObject (vdshwprv.h)
description: The IEnumVdsObject (vdshwprv.h) interface enumerates through a set of VDS objects of a given type.
helpviewer_keywords: ["IEnumVdsObject","IEnumVdsObject interface [VDS]","IEnumVdsObject interface [VDS]","described","base.ienumvdsobject","vds/IEnumVdsObject","vdshwprv/IEnumVdsObject"]
old-location: base\ienumvdsobject.htm
tech.root: base
ms.assetid: 08379071-b3cc-495a-bc8e-ad6cfacd432c
ms.date: 08/08/2022
ms.keywords: IEnumVdsObject, IEnumVdsObject interface [VDS], IEnumVdsObject interface [VDS],described, base.ienumvdsobject, vds/IEnumVdsObject, vdshwprv/IEnumVdsObject
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
 - IEnumVdsObject
 - vdshwprv/IEnumVdsObject
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
 - IEnumVdsObject
---

# IEnumVdsObject interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Enumerates through a 
   set of VDS objects of a given type. Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, 
   disk packs, disks, volumes, or volume plexes.

## -inheritance

The <b>IEnumVdsObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumVdsObject</b> also has these types of members:

## -see-also

<a href="/windows/desktop/VDS/helper-objects">Helper Objects</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>
