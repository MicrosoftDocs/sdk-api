---
UID: NF:gpmgmt.IGPMStarterGPOBackupCollection.get__NewEnum
title: IGPMStarterGPOBackupCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMstarterGPOBackupCollection.get__NewEnum)
helpviewer_keywords: ["IGPMStarterGPOBackupCollection.get__NewEnum","IGPMStarterGPOBackupCollection::get__NewEnum","IGPMstarterGPOBackupCollection interface [GPMC]","get__NewEnum method","IGPMstarterGPOBackupCollection::get__NewEnum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMstarterGPOBackupCollection interface","gpmc.igpmstartergpobackupcollection_get__newenum","gpmgmt/IGPMstarterGPOBackupCollection::get__NewEnum"]
old-location: gpmc\igpmstartergpobackupcollection_get__newenum.htm
tech.root: gpmc
ms.assetid: 87748dba-fe77-43a5-a9d1-8e068b96e197
ms.date: 12/05/2018
ms.keywords: IGPMStarterGPOBackupCollection.get__NewEnum, IGPMStarterGPOBackupCollection::get__NewEnum, IGPMstarterGPOBackupCollection interface [GPMC],get__NewEnum method, IGPMstarterGPOBackupCollection::get__NewEnum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMstarterGPOBackupCollection interface, gpmc.igpmstartergpobackupcollection_get__newenum, gpmgmt/IGPMstarterGPOBackupCollection::get__NewEnum
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
req.redist: GPMC on Windows Server 2008 or Windows Vista
ms.custom: 19H1
f1_keywords:
 - IGPMStarterGPOBackupCollection::get__NewEnum
 - gpmgmt/IGPMStarterGPOBackupCollection::get__NewEnum
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
 - IGPMstarterGPOBackupCollection.get__NewEnum
---

# IGPMStarterGPOBackupCollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMTmplBackup [out]

Pointer to an IEnumVARIANT interface of an enumerator object for the collection.  IEnumVARIANT provides a number of methods that you can use to iterate through the collection. For more information about IEnumVARIANT, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">IGPMStarterGPOBackupCollection</a>
