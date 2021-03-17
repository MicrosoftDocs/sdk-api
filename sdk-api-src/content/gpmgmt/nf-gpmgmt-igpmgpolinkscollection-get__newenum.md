---
UID: NF:gpmgmt.IGPMGPOLinksCollection.get__NewEnum
title: IGPMGPOLinksCollection::get__NewEnum (gpmgmt.h)
description: The get_NewEnum method retrieves an enumerator for the collection.
helpviewer_keywords: ["IGPMGPOLinksCollection interface [GPMC]","get__NewEnum method","IGPMGPOLinksCollection.get__NewEnum","IGPMGPOLinksCollection::get__NewEnum","_win32_igpmgpolinkscollection_get__newenum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMGPOLinksCollection interface","gpmc.igpmgpolinkscollection_get__newenum","gpmgmt/IGPMGPOLinksCollection::get__NewEnum"]
old-location: gpmc\igpmgpolinkscollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 953735c2-01d7-45e1-8417-6b18128de530
ms.date: 12/05/2018
ms.keywords: IGPMGPOLinksCollection interface [GPMC],get__NewEnum method, IGPMGPOLinksCollection.get__NewEnum, IGPMGPOLinksCollection::get__NewEnum, _win32_igpmgpolinkscollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMGPOLinksCollection interface, gpmc.igpmgpolinkscollection_get__newenum, gpmgmt/IGPMGPOLinksCollection::get__NewEnum
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
 - IGPMGPOLinksCollection::get__NewEnum
 - gpmgmt/IGPMGPOLinksCollection::get__NewEnum
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
 - IGPMGPOLinksCollection.get__NewEnum
---

# IGPMGPOLinksCollection::get__NewEnum


## -description

The <b>get_NewEnum</b> method retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMLinks [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolink">IGPMGPOLink</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolinkscollection">IGPMGPOLinksCollection</a>