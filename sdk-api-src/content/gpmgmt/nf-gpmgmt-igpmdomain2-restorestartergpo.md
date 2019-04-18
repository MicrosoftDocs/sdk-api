---
UID: NF:gpmgmt.IGPMDomain2.RestoreStarterGPO
title: IGPMDomain2::RestoreStarterGPO (gpmgmt.h)
author: windows-sdk-content
description: Restores the Starter Group Policy object (GPO) from a GPMStarterGPOBackup object.
old-location: gpmc\igpmdomain2_restorestartergpo.htm
tech.root: gpmc
ms.assetid: e91a3540-7f1b-4843-9b5e-4dcd837dc0f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGPMDomain2 interface [GPMC],RestoreStarterGPO method, IGPMDomain2.RestoreStarterGPO, IGPMDomain2::RestoreStarterGPO, RestoreStarterGPO, RestoreStarterGPO method [GPMC], RestoreStarterGPO method [GPMC],IGPMDomain2 interface, gpmc.igpmdomain2_restorestartergpo, gpmgmt/IGPMDomain2::RestoreStarterGPO
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
 - gpmgmt.dll
api_name:
 - IGPMDomain2.RestoreStarterGPO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMDomain2::RestoreStarterGPO


## -description


Restores the Starter Group Policy object (GPO) from a 
<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> object. You can restore a Starter GPO only to the domain in which the Starter GPO was originally created. This is because the operation restores the Starter GPO with its original Starter GPO ID and policy settings.


## -parameters




### -param pIGPMTmplBackup [in]

Pointer to the <a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> object to restore.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the restore operation. The caller must create this interface and then pass the interface pointer in this parameter to receive asynchronous notifications. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications. The method runs asynchronously if  this parameter is not <b>NULL</b>, and the method runs synchronously if <b>NULL</b>.


### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the restore operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface that represents the result of the restore operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/5ce7a7b4-e1c0-4e76-98c2-41462ec4ea17">IGPMstarterGPO</a> interface and to an 
<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface.


#### - objGPMStarterGPOBackup [in]


<a href="https://msdn.microsoft.com/b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9">GPMStarterGPOBackup</a> object that corresponds to the Starter GPO to restore.


## -returns



<h3>C++</h3>
 Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs. 

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">GPMResult</a> object.




## -remarks



A restore operation returns the contents of a specific GPO to the status it had when the backup was performed.

You must check the code that is returned by the 
<a href="https://msdn.microsoft.com/814c59b7-47bc-4757-997e-95ca578f544a">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.




## -see-also




<a href="https://msdn.microsoft.com/5abfea14-0cb9-46ea-915c-93a8d8b2477b">IGPMDomain2</a>
 

 

