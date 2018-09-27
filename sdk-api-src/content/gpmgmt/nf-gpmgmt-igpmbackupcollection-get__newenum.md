---
UID: NF:gpmgmt.IGPMBackupCollection.get__NewEnum
title: IGPMBackupCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmbackupcollection_get__newenum.htm
tech.root: GPMC
ms.assetid: cad0ead4-cfd4-450e-95f3-9a52774b6c0e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IGPMBackupCollection interface [GPMC],get__NewEnum method, IGPMBackupCollection.get__NewEnum, IGPMBackupCollection::get__NewEnum, _win32_igpmbackupcollection_get__newenum, get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC],IGPMBackupCollection interface, gpmc.igpmbackupcollection_get__newenum, gpmgmt/IGPMBackupCollection::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackupCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

