---
UID: NF:gpmgmt.IGPMCSECollection.get__NewEnum
title: IGPMCSECollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMCSECollection.get__NewEnum)
helpviewer_keywords: ["IGPMCSECollection interface [GPMC]","get__NewEnum method","IGPMCSECollection.get__NewEnum","IGPMCSECollection::get__NewEnum","_win32_igpmcsecollection_get__newenum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMCSECollection interface","gpmc.igpmcsecollection_get__newenum","gpmgmt/IGPMCSECollection::get__NewEnum"]
old-location: gpmc\igpmcsecollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 2c3b9e29-6c46-4ed1-9e60-2e71d8792020
ms.date: 12/05/2018
ms.keywords: IGPMCSECollection interface [GPMC],get__NewEnum method, IGPMCSECollection.get__NewEnum, IGPMCSECollection::get__NewEnum, _win32_igpmcsecollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMCSECollection interface, gpmc.igpmcsecollection_get__newenum, gpmgmt/IGPMCSECollection::get__NewEnum
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
 - IGPMCSECollection::get__NewEnum
 - gpmgmt/IGPMCSECollection::get__NewEnum
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
 - IGPMCSECollection.get__NewEnum
---

# IGPMCSECollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMCSEs [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmcsecollection">IGPMCSECollection</a>
