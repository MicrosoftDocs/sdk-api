---
UID: NF:gpmgmt.IGPMStarterGPOBackupCollection.get__NewEnum
title: IGPMStarterGPOBackupCollection::get__NewEnum method
author: windows-driver-content
description: Retrieves an enumerator for the collection.
old-location: gpmc\igpmstartergpobackupcollection_get__newenum.htm
old-project: GPMC
ms.assetid: 87748dba-fe77-43a5-a9d1-8e068b96e197
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IGPMStarterGPOBackupCollection, IGPMStarterGPOBackupCollection::get__NewEnum, IGPMstarterGPOBackupCollection interface [GPMC], get__NewEnum method, IGPMstarterGPOBackupCollection::get__NewEnum, get__NewEnum method [GPMC], get__NewEnum method [GPMC], IGPMstarterGPOBackupCollection interface, get__NewEnum,IGPMStarterGPOBackupCollection.get__NewEnum, gpmc.igpmstartergpobackupcollection_get__newenum, gpmgmt/IGPMstarterGPOBackupCollection::get__NewEnum
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMstarterGPOBackupCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPOBackupCollection::get__NewEnum method


## -description


Retrieves an enumerator for the collection.


## -parameters




### -param ppIGPMTmplBackup [out]

Pointer to an IEnumVARIANT interface of an enumerator object for the collection.  IEnumVARIANT provides a number of methods that you can use to iterate through the collection. For more information about IEnumVARIANT, see the COM documentation in the Platform SDK.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">IGPMStarterGPOBackupCollection</a>
 

 

