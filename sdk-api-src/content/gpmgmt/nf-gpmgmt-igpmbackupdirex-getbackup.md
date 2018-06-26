---
UID: NF:gpmgmt.IGPMBackupDirEx.GetBackup
title: IGPMBackupDirEx::GetBackup
author: windows-sdk-content
description: Retrieves the GPMBackup or GPMStarterGPOBackup object with the specified backup ID. The backup ID is a GUID. The backup ID is the ID of the backed-up Group Policy object (GPO), not the ID of the GPO.
old-location: gpmc\igpmbackupdirex_getbackup.htm
old-project: GPMC
ms.assetid: d1c6ead9-882d-4041-9586-f08a83f4c9b0
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetBackup, GetBackup method [GPMC], GetBackup method [GPMC],IGPMBackupDirEx interface, IGPMBackupDirEx interface [GPMC],GetBackup method, IGPMBackupDirEx.GetBackup, IGPMBackupDirEx::GetBackup, gpmc.igpmbackupdirex_getbackup, gpmgmt/IGPMBackupDirEx::GetBackup
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
 - gpmgmt.dll
api_name:
 - IGPMBackupDirEx.GetBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMBackupDirEx::GetBackup


## -description


Retrieves the <b>GPMBackup</b> or <b>GPMStarterGPOBackup</b> object with the specified backup ID. The backup ID is a GUID. The backup ID is the ID of the backed-up Group Policy object (GPO), not the ID of the GPO.


## -parameters




### -param bstrID [in]

ID of the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object to open.


### -param pvarBackup [out]

Pointer to the 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> or <b>IGPMStarterGPOBackup</b> interface for the ID specified.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
 

 

