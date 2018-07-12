---
UID: NF:gpmgmt.IGPMGPO.CopyTo
title: IGPMGPO::CopyTo
author: windows-sdk-content
description: Copies the current Group Policy object (GPO) to the specified domain and then returns a pointer to the copy of the GPO.
old-location: gpmc\igpmgpo_copyto.htm
old-project: gpmc
ms.assetid: 17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: CopyTo, CopyTo method [GPMC], CopyTo method [GPMC],GPMGPO object, CopyTo method [GPMC],IGPMGPO interface, GPMGPO object [GPMC],CopyTo method, IGPMGPO interface [GPMC],CopyTo method, IGPMGPO.CopyTo, IGPMGPO::CopyTo, _win32_igpmgpo_copyto, gpmc.igpmgpo_copyto, gpmgmt/IGPMGPO::CopyTo
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
 - IGPMGPO.CopyTo
 - GPMGPO.CopyTo
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::CopyTo


## -description


Copies the current Group Policy object (GPO) to the specified domain and then returns a pointer to the copy of 
    the GPO. This method copies the policy settings from the current GPO to the new GPO. The new GPO has a new GPO ID. 
    The new GPO gets either the default GPO 
    <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">access control lists</a> (ACLs) or the ACLs from the 
    source GPO. The ACL that the new GPO gets depends on the value of the <i>lFlags</i> parameter. 
    This method does not link any scopes of management (SOMs) to the new GPO.


## -parameters




### -param lFlags [in]

Specifies the options to use for security principal and path mapping. For more information, see 
      <a href="https://msdn.microsoft.com/f4a14a75-50f2-4f42-9c11-fc15856a469c">Copying and Importing GPOs Across Domains</a>. 
      The following options are defined.



#### 0

Map the security principal and the Universal Naming Convention (UNC) path from the migration table if 
        specified. If there is no entry corresponding to Security principal or UNCPath, keep the setting that contains the Security principal or UNC Path as it is. Do not copy security on the GPO and Software Installation Package objects. This is the default value of this parameter.



#### GPM_MIGRATIONTABLE_ONLY

Map the security principals and the UNC paths by using the information specified in the migration table 
        only. If a setting is found that cannot be mapped through the migration table, the method fails and returns an 
        error code.



#### GPM_PROCESS_SECURITY

Copy the specified permissions (DACLs) on the GPO.


### -param pIGPMDomain [in]

Domain to which the GPO is copied.


### -param pvarNewDisplayName [in, optional]

Display name for the copied GPO. A display name is assigned if the <b>VARIANT</b> structure does not contain a <b>BSTR</b> or if the <i>pvarNewDisplayName</i> parameter is <b>NULL</b>.


### -param pvarMigrationTable [in, optional]

Pointer to the <a href="https://msdn.microsoft.com/c80c76b0-8589-4ecb-b9bf-6b8377fa98dd">IGPMMigrationTable</a> interface to use for mapping. This parameter can be <b>NULL</b>.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface. This interface allows the client to receive status notifications about the progress of the copy operation. This parameter must be <b>NULL</b> if the client does not receive asynchronous notifications.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface that represents the result of the copy operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface and to an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


#### - MigrationTable [in, optional]

Path of a file that contains the migration table to use for mapping.


#### - NewGpoName [in, optional]

Display name to be put on the copied GPO.


#### - gpmDomain [in]


<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">GPMDomain</a> object of the domain to which the GPO is copied.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -remarks



The new GPO that is created by using this method is unlinked because a copy operation does not transfer links.

You must check the code that is returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.

An import operation is similar to a copy operation, except that in an import operation, the source GPO must be in the file system and the destination must be an existing GPO in Active Directory. In contrast, for a copy operation, the source GPO must be in Active Directory. A copy operation creates a new destination GPO. An import operation transfers only policy settings. An import operation does not modify the GPO ID or the 
<a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">ACLs</a> on the destination GPO. And, an import operation does not modify any links that point to the destination GPO or to an associated Windows Management Instrumentation (WMI) filter. For more information about importing GPOs, see 
<a href="https://msdn.microsoft.com/3b16eefb-89af-408b-a84c-c8ab958b4cc7">IGPMGPO::Import</a>.

For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

