---
UID: NF:gpmgmt.IGPMStarterGPOCollection.get__NewEnum
title: IGPMStarterGPOCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMStarterGPOCollection.get__NewEnum)
helpviewer_keywords: ["IGPMStarterGPOCollection interface [GPMC]","get__NewEnum method","IGPMStarterGPOCollection.get__NewEnum","IGPMStarterGPOCollection::get__NewEnum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMStarterGPOCollection interface","gpmc.igpmstartergpocollection_get__newenum","gpmgmt/IGPMStarterGPOCollection::get__NewEnum"]
old-location: gpmc\igpmstartergpocollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 0e0e6360-46a9-49ff-9eb9-0ea708258ebb
ms.date: 12/05/2018
ms.keywords: IGPMStarterGPOCollection interface [GPMC],get__NewEnum method, IGPMStarterGPOCollection.get__NewEnum, IGPMStarterGPOCollection::get__NewEnum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMStarterGPOCollection interface, gpmc.igpmstartergpocollection_get__newenum, gpmgmt/IGPMStarterGPOCollection::get__NewEnum
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
 - IGPMStarterGPOCollection::get__NewEnum
 - gpmgmt/IGPMStarterGPOCollection::get__NewEnum
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
 - IGPMStarterGPOCollection.get__NewEnum
---

# IGPMStarterGPOCollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMTemplates [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpocollection">IGPMStarterGPOCollection</a>
