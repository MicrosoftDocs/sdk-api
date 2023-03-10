---
UID: NF:gpmgmt.IGPMSecurityInfo.get__NewEnum
title: IGPMSecurityInfo::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMSecurityInfo.get__NewEnum)
helpviewer_keywords: ["IGPMSecurityInfo interface [GPMC]","get__NewEnum method","IGPMSecurityInfo.get__NewEnum","IGPMSecurityInfo::get__NewEnum","_win32_igpmsecurityinfo_get__newenum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMSecurityInfo interface","gpmc.igpmsecurityinfo_get__newenum","gpmgmt/IGPMSecurityInfo::get__NewEnum"]
old-location: gpmc\igpmsecurityinfo_get__newenum.htm
tech.root: gpmc
ms.assetid: f8dc2ee1-d1cb-4e7a-abf4-1a388320b681
ms.date: 12/05/2018
ms.keywords: IGPMSecurityInfo interface [GPMC],get__NewEnum method, IGPMSecurityInfo.get__NewEnum, IGPMSecurityInfo::get__NewEnum, _win32_igpmsecurityinfo_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMSecurityInfo interface, gpmc.igpmsecurityinfo_get__newenum, gpmgmt/IGPMSecurityInfo::get__NewEnum
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
 - IGPMSecurityInfo::get__NewEnum
 - gpmgmt/IGPMSecurityInfo::get__NewEnum
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
 - IGPMSecurityInfo.get__NewEnum
---

# IGPMSecurityInfo::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppEnum [out, retval]

Pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface of an enumerator object for the collection. <b>IEnumVARIANT</b> provides a number of methods that you can use to iterate through the collection.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>
