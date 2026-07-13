---
UID: NF:gpmgmt.IGPMMapEntryCollection.get__NewEnum
title: IGPMMapEntryCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMMapEntryCollection.get__NewEnum)
helpviewer_keywords: ["IGPMMapEntryCollection interface [GPMC]","get__NewEnum method","IGPMMapEntryCollection.get__NewEnum","IGPMMapEntryCollection::get__NewEnum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMMapEntryCollection interface","gpmc.igpmmapentrycollection_get__newenum","gpmgmt/IGPMMapEntryCollection::get__NewEnum"]
old-location: gpmc\igpmmapentrycollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 7c169028-e87f-45d2-aadd-c403699cfd73
ms.date: 12/05/2018
ms.keywords: IGPMMapEntryCollection interface [GPMC],get__NewEnum method, IGPMMapEntryCollection.get__NewEnum, IGPMMapEntryCollection::get__NewEnum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMMapEntryCollection interface, gpmc.igpmmapentrycollection_get__newenum, gpmgmt/IGPMMapEntryCollection::get__NewEnum
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
 - IGPMMapEntryCollection::get__NewEnum
 - gpmgmt/IGPMMapEntryCollection::get__NewEnum
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
 - IGPMMapEntryCollection.get__NewEnum
---

# IGPMMapEntryCollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param pVal [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmessage">IGPMStatusMessage</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
