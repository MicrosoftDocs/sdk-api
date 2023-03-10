---
UID: NF:gpmgmt.IGPMGPOCollection.get__NewEnum
title: IGPMGPOCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMGPOCollection.get__NewEnum)
helpviewer_keywords: ["IGPMGPOCollection interface [GPMC]","get__NewEnum method","IGPMGPOCollection.get__NewEnum","IGPMGPOCollection::get__NewEnum","_win32_igpmgpocollection_get__newenum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMGPOCollection interface","gpmc.igpmgpocollection_get__newenum","gpmgmt/IGPMGPOCollection::get__NewEnum"]
old-location: gpmc\igpmgpocollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 7db1ec65-9850-4f14-b223-a7decc7648a6
ms.date: 12/05/2018
ms.keywords: IGPMGPOCollection interface [GPMC],get__NewEnum method, IGPMGPOCollection.get__NewEnum, IGPMGPOCollection::get__NewEnum, _win32_igpmgpocollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMGPOCollection interface, gpmc.igpmgpocollection_get__newenum, gpmgmt/IGPMGPOCollection::get__NewEnum
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMGPOCollection::get__NewEnum
 - gpmgmt/IGPMGPOCollection::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMGPOCollection.get__NewEnum
---

# IGPMGPOCollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMGPOs [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>
