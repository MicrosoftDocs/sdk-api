---
UID: NF:gpmgmt.IGPMBackupCollection.get__NewEnum
title: IGPMBackupCollection::get__NewEnum (gpmgmt.h)
description: Retrieves an enumerator for the collection. (IGPMBackupCollection.get__NewEnum)
helpviewer_keywords: ["IGPMBackupCollection interface [GPMC]","get__NewEnum method","IGPMBackupCollection.get__NewEnum","IGPMBackupCollection::get__NewEnum","_win32_igpmbackupcollection_get__newenum","get__NewEnum","get__NewEnum method [GPMC]","get__NewEnum method [GPMC]","IGPMBackupCollection interface","gpmc.igpmbackupcollection_get__newenum","gpmgmt/IGPMBackupCollection::get__NewEnum"]
old-location: gpmc\igpmbackupcollection_get__newenum.htm
tech.root: gpmc
ms.assetid: cad0ead4-cfd4-450e-95f3-9a52774b6c0e
ms.date: 12/05/2018
ms.keywords: IGPMBackupCollection interface [GPMC],get__NewEnum method, IGPMBackupCollection.get__NewEnum, IGPMBackupCollection::get__NewEnum, _win32_igpmbackupcollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMBackupCollection interface, gpmc.igpmbackupcollection_get__newenum, gpmgmt/IGPMBackupCollection::get__NewEnum
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
 - IGPMBackupCollection::get__NewEnum
 - gpmgmt/IGPMBackupCollection::get__NewEnum
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
 - IGPMBackupCollection.get__NewEnum
---

# IGPMBackupCollection::get__NewEnum


## -description

Retrieves an enumerator for the collection.

## -parameters

### -param ppIGPMBackup [out]

Pointer to an <b>IEnumVARIANT</b> interface of an enumerator object for the collection.  <b>IEnumVARIANT</b> provides several methods that you can use to iterate through the collection. For more information about <b>IEnumVARIANT</b>, see the COM documentation in the Platform SDK.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
