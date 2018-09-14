---
UID: NF:gpmgmt.IGPMStarterGPO.CopyTo
title: IGPMStarterGPO::CopyTo
author: windows-sdk-content
description: The CopyTo method copies the current Starter GPO and returns a pointer to the copy of the Starter GPO.
old-location: gpmc\igpmstartergpo_copyto.htm
tech.root: GPMC
ms.assetid: 28639323-5253-4f63-b1b1-4fd75abaa2b4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CopyTo, CopyTo method [GPMC], CopyTo method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],CopyTo method, IGPMStarterGPO.CopyTo, IGPMStarterGPO::CopyTo, gpmc.igpmstartergpo_copyto, gpmgmt/IGPMStarterGPO::CopyTo
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
 - gpmgmt.dll
api_name:
 - IGPMStarterGPO.CopyTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPO::CopyTo


## -description


The <b>CopyTo</b> method copies the current Starter GPO and returns a pointer to the copy of the Starter GPO.  The method copies all the contents of the Starter GPO but creates the new Starter GPO with the default new Starter GPO delegation settings.  Copying a system Starter GPO creates a new custom Starter GPO.


## -parameters




### -param pvarNewDisplayName [in, optional]

Display name to be put on the copied Starter GPO. A display name is assigned if the <b>VARIANT</b> structure does not contain a <b>BSTR</b>, or if <i>pvarNewDisplayName</i> is <b>NULL</b>.


### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the copy operation. This parameter must be <b>NULL</b> if the client does not receive asynchronous notifications.


### -param pvarGPMCancel [in, optional]

Receives a pointer to an 
<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.


### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="https://msdn.microsoft.com/0228ed1a-3a8f-486a-9dd8-806ca35c649e">IGPMResult</a> interface that represents the result of the copy operation. That interface contains pointers to an 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> interface and an 
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
 

 

