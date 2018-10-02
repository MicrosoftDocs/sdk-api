---
UID: NF:gpmgmt.IGPMGPO.Import
title: IGPMGPO::Import
author: windows-sdk-content
description: Imports the policy settings from the specified GPMBackup object.
old-location: gpmc\igpmgpo_import.htm
tech.root: GPMC
ms.assetid: 3b16eefb-89af-408b-a84c-c8ab958b4cc7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMGPO object [GPMC],Import method, IGPMGPO interface [GPMC],Import method, IGPMGPO.Import, IGPMGPO::Import, Import, Import method [GPMC], Import method [GPMC],GPMGPO object, Import method [GPMC],IGPMGPO interface, _win32_igpmgpo_import, gpmc.igpmgpo_import, gpmgmt/IGPMGPO::Import
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
 - IGPMGPO.Import
 - GPMGPO.Import
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::Import


## -description


Imports the policy settings from the specified 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object. An import operation transfers the policy settings from a backed-up GPO in the file system to a GPO in the Active Directory. The operation erases any previous policy settings in the destination GPO. The source GPO can be any backed-up GPO in the file system and the destination GPO must be an existing GPO in the Active Directory.


## -parameters




### -param lFlags [in]

Specifies the options to use for security principal and path mapping. The following options are defined. For more information, see 
<a href="https://msdn.microsoft.com/f4a14a75-50f2-4f42-9c11-fc15856a469c">Copying and Importing GPOs Across Domains</a>.



#### 0

Map the Security principal and UNC path from the migration table if specified. If there is no entry corresponding to Security principal or UNCPath, keep the setting containing that Security principal or UNC Path as it is. Do not copy security on the GPO and Software Installation Package objects. This is the default value for this parameter.



#### GPM_MIGRATIONTABLE_ONLY

Map the security principals and UNC paths using the information specified in the migration table only. If a setting is found that cannot be mapped through the migration table, the method fails and returns an error code.


### -param pIGPMBackup [in]

Pointer to the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object from which settings should be imported.


### -param pvarMigrationTable [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/c80c76b0-8589-4ecb-b9bf-6b8377fa98dd">IGPMMigrationTable</a> to use for mapping.  This parameter can be <b>NULL</b>.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the import operation. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the import operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface representing the result of the import operation. That interface contains a pointer to an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface and an 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface.


#### - MigrationTable [in, optional]

Path of a file that contains the migration table to use for mapping.


#### - gpmBackup [in]


<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object from which settings should be imported.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -remarks



An import operation only transfers policy settings. It erases any existing settings in the GPO. An import does not modify the GPO ID or the <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">ACLs</a> on the destination GPO, nor does it modify any links that point to the destination GPO or to an associated WMI filter.

<div class="alert"><b>Note</b>  An import operation is similar but different than a copy operation. For an import operation, the source GPO must be in the file system and the destination must be an existing GPO in Active Directory. For a copy operation, the source GPO must be in the Active Directory  and the copy creates a new destination GPO. For more information about copying GPOs, see 
<a href="https://msdn.microsoft.com/17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07">IGPMGPO::CopyTo</a>.</div>
<div> </div>
Note that you must check the code returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code; otherwise it returns a failure code.

For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

