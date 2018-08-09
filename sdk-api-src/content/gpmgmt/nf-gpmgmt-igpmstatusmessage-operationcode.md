---
UID: NF:gpmgmt.IGPMStatusMessage.OperationCode
title: IGPMStatusMessage::OperationCode
author: windows-sdk-content
description: Returns a code related to the GPMC operation.
old-location: gpmc\igpmstatusmessage_operationcode.htm
old-project: GPMC
ms.assetid: f99dc90a-fabe-40fb-8289-36501a68b11d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMStatusMessage class [GPMC],OperationCode method, IGPMStatusMessage interface [GPMC],OperationCode method, IGPMStatusMessage.OperationCode, IGPMStatusMessage::OperationCode, OperationCode, OperationCode method [GPMC], OperationCode method [GPMC],GPMStatusMessage class, OperationCode method [GPMC],IGPMStatusMessage interface, _win32_igpmstatusmessage_operationcode, gpmc.igpmstatusmessage_operationcode, gpmgmt/IGPMStatusMessage::OperationCode
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
 - IGPMStatusMessage.OperationCode
 - GPMStatusMessage.OperationCode
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMStatusMessage::OperationCode


## -description


Returns a code related to the GPMC operation. The code corresponds to warnings or other errors that occurred during the operation. In the case of warnings, the operation continues. In the case of other errors, the operation stops.

The operation codes are internal identifiers that are defined in Gpmgmt.dll. You can extract a text description of the operation code by using the  <a href="https://msdn.microsoft.com/8d736e30-760d-43fa-ab5d-d05dc679bfbb">Message property</a> of <a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">IGPMStatusMessage</a> or by using <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>.


## -parameters






## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -see-also




<a href="https://msdn.microsoft.com/8570d40c-25c2-405c-b52a-dae6c0eb50e0">IGPMStatusMessage</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

