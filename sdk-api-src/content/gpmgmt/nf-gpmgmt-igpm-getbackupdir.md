---
UID: NF:gpmgmt.IGPM.GetBackupDir
title: IGPM::GetBackupDir
author: windows-sdk-content
description: Creates and returns a GPMBackupDir object, which you can use to access the GPMBackup and GPMBackupCollection objects.
old-location: gpmc\igpm_getbackupdir.htm
old-project: GPMC
ms.assetid: 4ffc8827-8427-4ee5-ad89-21f821d16d97
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPM class [GPMC],GetBackupDir method, GetBackupDir, GetBackupDir method [GPMC], GetBackupDir method [GPMC],GPM class, GetBackupDir method [GPMC],IGPM interface, IGPM interface [GPMC],GetBackupDir method, IGPM.GetBackupDir, IGPM::GetBackupDir, _win32_igpm_getbackupdir, gpmc.igpm_getbackupdir, gpmgmt/IGPM::GetBackupDir
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPM.GetBackupDir
 - GPM.GetBackupDir
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::GetBackupDir


## -description


Creates and returns a <a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDir</a> object, which you can use to access 
the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> and 
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> objects.


## -parameters




### -param bstrBackupDir [in]

Required.  The name of the file system directory that contains the Group Policy object (GPO) backups. The directory must already exist.


### -param pIGPMBackupDir [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs

<h3>JScript</h3>
Returns a reference to a <b>GPMBackupDir</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMBackupDir</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

