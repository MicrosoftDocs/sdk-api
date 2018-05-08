---
UID: NF:gpmgmt.IGPM2.GetBackupDirEx
title: IGPM2::GetBackupDirEx
author: windows-driver-content
description: For a Group Policy object (GPO), the GetBackupDirEx method creates and returns a GPMBackupDirEx object, which you can use to access a GPMBackup or GPMBackupCollection object.
old-location: gpmc\igpm2_getbackupdirex.htm
old-project: GPMC
ms.assetid: 2fe4ea93-6668-4534-b72e-71b1062db627
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetBackupDirEx, GetBackupDirEx method [GPMC], GetBackupDirEx method [GPMC],IGPM2 interface, IGPM2 interface [GPMC],GetBackupDirEx method, IGPM2.GetBackupDirEx, IGPM2::GetBackupDirEx, gpmc.igpm2_getbackupdirex, gpmgmt/IGPM2::GetBackupDirEx
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
-	gpmgmt.dll
api_name:
-	IGPM2.GetBackupDirEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM2::GetBackupDirEx


## -description


For a Group Policy object (GPO), the <b>GetBackupDirEx</b> method creates and returns a <a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDirEx</a> object, which you can use to access 
a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> or <a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> object.

For a Starter Group Policy object, the <b>GetBackupDirEx</b> method creates and returns a <a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">GPMBackupDirEx</a> object, which you can use to access 
a <a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> or <a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">GPMStarterGPOBackupCollection</a> object.


## -parameters




### -param bstrBackupDir [in]

Required. The name of the file system directory containing the Group Policy object (GPO) backups. Note that the directory must already exist.


### -param backupDirType [in]

Determines whether the back up is for a Starter Group Policy object or a Group Policy object.


### -param ppIGPMBackupDirEx [out, retval]

Address of a pointer to the   <a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">GPMBackupDirEx</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">GPMBackupDirEx</a> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/f9cd432a-3974-4fc4-9e32-1d8e2df1601c">IGPM2</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>



<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">IGPMStarterGPOBackup</a>



<a href="https://msdn.microsoft.com/df9f29d0-8636-4393-8f7e-c9e22f3692f5">IGPMStarterGPOBackupCollection</a>
 

 

