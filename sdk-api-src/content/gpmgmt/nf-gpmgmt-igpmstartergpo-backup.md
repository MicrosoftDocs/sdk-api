---
UID: NF:gpmgmt.IGPMStarterGPO.Backup
title: IGPMStarterGPO::Backup
author: windows-sdk-content
description: Creates a backup of the current Starter GPO.
old-location: gpmc\igpmstartergpo_backup.htm
old-project: GPMC
ms.assetid: bf419f56-803f-44c2-ae08-7e428940f79d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Backup, Backup method [GPMC], Backup method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],Backup method, IGPMStarterGPO.Backup, IGPMStarterGPO::Backup, gpmc.igpmstartergpo_backup, gpmgmt/IGPMStarterGPO::Backup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.redist: 
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
 - IGPMStarterGPO.Backup
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStarterGPO::Backup


## -description


Creates a backup of the current Starter GPO.


## -parameters




### -param bstrBackupDir [in]

Name of the file system directory in which the <b>GPMStarterGPOBackup</b> object should be stored.  The directory must already exist.  Use a null-terminated string.


### -param bstrComment [in]

Comment to associate with the <b>GPMStarterGPOBackup</b> object.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the backup operation. The method runs synchronously if this parameter is <b>NULL</b>. The method runs asynchronously if this parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the backup operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface representing the result of the backup operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface and an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


## -returns



Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

For more information, see the following Remarks section.




## -remarks



Note that you must check the code returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code; otherwise it returns a failure code.




## -see-also




<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMStarterGPO</a>
 

 

