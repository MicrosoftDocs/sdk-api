---
UID: NF:gpmgmt.IGPMGPO.Backup
title: IGPMGPO::Backup
author: windows-sdk-content
description: Backs up a Group Policy object (GPO) to the specified directory.
old-location: gpmc\igpmgpo_backup.htm
tech.root: GPMC
ms.assetid: 5ba8d2f7-4989-4882-9ceb-4f77b8745442
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Backup, Backup method [GPMC], Backup method [GPMC],GPMGPO object, Backup method [GPMC],IGPMGPO interface, GPMGPO object [GPMC],Backup method, IGPMGPO interface [GPMC],Backup method, IGPMGPO.Backup, IGPMGPO::Backup, _win32_igpmgpo_backup, gpmc.igpmgpo_backup, gpmgmt/IGPMGPO::Backup
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
 - IGPMGPO.Backup
 - GPMGPO.Backup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::Backup


## -description


Backs up a Group Policy object (GPO) to the specified directory. A backup operation transfers the contents of a GPO from the Active Directory directory service to the file system. The backup includes the policy settings, the GPO ID, and any 
<a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">access control lists</a> (ACLs) that are associated with the GPO. This method is also used for exporting GPOs to the file system.


## -parameters




### -param bstrBackupDir [in]

Name of the file system directory in which the  <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object should be stored. The directory must already exist.


### -param bstrComment [in]

Comment to associate with the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the backup operation. The method runs synchronously if this parameter is <b>NULL</b>. The method runs asynchronously if this parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the backup operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface that represents the result of the backup operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interface and to an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -remarks



A GPO that has been backed-up (also called exported) can be restored to the Active Directory by calling the 
<a href="https://msdn.microsoft.com/8e202ea1-ca5c-4757-950b-ea1802699b68">IGPMDomain::RestoreGPO</a> method or imported into another existing GPO using the 
<a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">IGPMGPO::Import</a> method, depending on the required result.

You must check the code that is returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one that is returned by this method to determine whether the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

