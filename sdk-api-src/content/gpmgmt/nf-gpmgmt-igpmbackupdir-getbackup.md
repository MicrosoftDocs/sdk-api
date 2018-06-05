---
UID: NF:gpmgmt.IGPMBackupDir.GetBackup
title: IGPMBackupDir::GetBackup
author: windows-sdk-content
description: Retrieves the GPMBackup object that has the specified backup ID (GUID). The backup ID is the ID of the backed-up GPO, not the ID of the GPO.
old-location: gpmc\igpmbackupdir_getbackup.htm
old-project: GPMC
ms.assetid: 45f286dc-fa60-4cfd-bdf0-bfeaf2a5a396
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMBackupDir object [GPMC],GetBackup method, GetBackup, GetBackup method [GPMC], GetBackup method [GPMC],GPMBackupDir object, GetBackup method [GPMC],IGPMBackupDir interface, IGPMBackupDir interface [GPMC],GetBackup method, IGPMBackupDir.GetBackup, IGPMBackupDir::GetBackup, _win32_igpmbackupdir_getbackup, gpmc.igpmbackupdir_getbackup, gpmgmt/IGPMBackupDir::GetBackup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMBackupDir.GetBackup
-	GPMBackupDir.GetBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMBackupDir::GetBackup


## -description


Retrieves the <b>GPMBackup</b> object that has the specified backup ID (GUID). The backup ID is the ID of the backed-up GPO, not the ID of the GPO.


## -parameters




### -param bstrID [in]

ID of the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> object to open.


### -param ppBackup [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface for the specified ID.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

