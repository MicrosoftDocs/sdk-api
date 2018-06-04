---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IGPMAsyncProgress::Status


## -description


The server calls this method to notify the client about the status of a Group Policy Management Console (GPMC) operation.


## -parameters




### -param lProgressNumerator [in]

Numerator of a fraction that represents the percent of the GPMC operation that is complete.


### -param lProgressDenominator [in]

Denominator of a fraction that represents the percent of the GPMC operation that is complete. The value of this parameter is proportional to the number of extensions in the Group Policy object (GPO), whether the GPO is a "live" GPO or a backed-up GPO. This value can be used to display the progress bar to the user.

In the GPMC user interface, the progress bar is divided into <i>lProgressDenominator</i> intervals. When <i>lProgressNumerator</i>==<i>lProgressDenominator</i> the operation is complete.


### -param hrStatus [in]

Status of the operation. If no error occurred, the value of the parameter is <b>S_OK</b>.


### -param pResult [in]

Result of the operation. 
This parameter is an interface pointer to the object that resulted from the GPMC operation. For example, it may be a pointer to a <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object or to  a <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object. This object is only returned when the operation is complete.


### -param ppIGPMStatusMsgCollection [in]

A pointer to the <a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a> interface that contains detailed status information about the operation. In cases where there are no errors, or if there are no detailed messages, Status passes in a null collection.


## -returns



This method has no return values.




## -remarks



This method must be implemented by the client.




## -see-also




<a href="https://msdn.microsoft.com/74b2bb04-6118-4fd1-83c0-3549db3f35f3">IGPMAsyncCancel</a>



<a href="https://msdn.microsoft.com/f48b90db-5984-4ea7-826b-6fbbf3c33788">IGPMAsyncProgress</a>
 

 

