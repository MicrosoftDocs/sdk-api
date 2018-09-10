---
UID: NF:gpmgmt.IGPMDomain.RestoreGPO
title: IGPMDomain::RestoreGPO
author: windows-sdk-content
description: Restores a Group Policy object (GPO) from a GPMBackup object.
old-location: gpmc\igpmdomain_restoregpo.htm
tech.root: GPMC
ms.assetid: 8e202ea1-ca5c-4757-950b-ea1802699b68
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMDomain object [GPMC],RestoreGPO method, IGPMDomain interface [GPMC],RestoreGPO method, IGPMDomain.RestoreGPO, IGPMDomain::RestoreGPO, RestoreGPO, RestoreGPO method [GPMC], RestoreGPO method [GPMC],GPMDomain object, RestoreGPO method [GPMC],IGPMDomain interface, _win32_igpmdomain_restoregpo, gpmc.igpmdomain_restoregpo, gpmgmt/IGPMDomain::RestoreGPO
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
 - IGPMDomain.RestoreGPO
 - GPMDomain.RestoreGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMDomain::RestoreGPO


## -description


Restores a Group Policy object (GPO) from a 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object. You can only restore a GPO to the domain in which the GPO was originally  created because the operation restores the GPO with its original GPO ID, policy settings, <a href="https://msdn.microsoft.com/c9aff246-fe11-4d82-b944-b10c3d9ae170">access control lists</a> (ACLs), and links to Windows Management Instrumentation (WMI) filters.


## -parameters




### -param pIGPMBackup [in]

Pointer to the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object to restore.


### -param lDCFlags [in]

Flags to use for validation. If this parameter is set to zero, the method validates the domain controller to determine whether the restore operation can be performed. If you specify <b>GPM_DONOT_VALIDATEDC</b>, the method does not validate the DC. This parameter is ignored for GPOs that do not include software policy settings. For more information about validation, see the "Remarks" section.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the restore operation. To receive asynchronous notifications, the caller must create this interface and then pass the interface pointer in this parameter. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications. The method will run asynchronously if  this parameter is not <b>NULL</b> and will run synchronously if <b>NULL</b>.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the restore operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface that represents the result of the restore operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface and an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


#### - objGPMBackup [in]


<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object that corresponds to the GPO to restore.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs. Returns <b>E_OPERATION_NOT_SUPPORTED_ONDC</b> if the current domain controller is running an old Windows Server version and the backed-up GPO contains software policy settings.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -remarks



A restore operation returns the contents of a specific GPO to the status it had when the backup was performed. A restore operation does not modify links to the GPO because they are attributes of a scope of management (SOM). A restore operation also does not modify WMI filters. However, because the link to a WMI filter is an attribute of the GPO, the restore operation restores the link to the WMI filter.

You must check the code that is returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.

As a best practice, we recommend that you validate the DC in a restore operation.




## -see-also




<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a>



<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

