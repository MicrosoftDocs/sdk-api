---
UID: NF:gpmgmt.IGPMMigrationTable.Add
title: IGPMMigrationTable::Add
author: windows-sdk-content
description: Adds entries from the IGPMGPO and IGPMBackup interfaces. The method updates any entries that are already present in the migration table.
old-location: gpmc\igpmmigrationtable_add.htm
tech.root: GPMC
ms.assetid: e7be82b5-acb5-4e08-9771-d2698df3d0df
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Add, Add method [GPMC], Add method [GPMC],GPMMigrationTable class, Add method [GPMC],IGPMMigrationTable interface, GPMMigrationTable class [GPMC],Add method, GPM_PROCESS_SECURITY, IGPMMigrationTable interface [GPMC],Add method, IGPMMigrationTable.Add, IGPMMigrationTable::Add, gpmc.igpmmigrationtable_add, gpmgmt/IGPMMigrationTable::Add
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
 - IGPMMigrationTable.Add
 - GPMMigrationTable.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMMigrationTable::Add


## -description


Adds entries from the <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> and <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interfaces. The method updates any entries that are already present in the migration table.


## -parameters




### -param lFlags [in]

This parameter must be one of the following values.



#### 0

Do not take security principals from the DACLs in the backup GPO or the live GPO.



#### GPM_PROCESS_SECURITY

Copy all the entries from the DACLs and settings.


### -param var [in]

Dispatch pointer to an <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> or <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface.


#### - gpm [in]

The <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> or <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c80c76b0-8589-4ecb-b9bf-6b8377fa98dd">IGPMMigrationTable</a>
 

 

