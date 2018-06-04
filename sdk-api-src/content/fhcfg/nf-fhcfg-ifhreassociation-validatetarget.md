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

# IFhReassociation::ValidateTarget


## -description


 This method checks whether a certain storage device or network share can be used as a File History default target and, thus, whether reassociation is possible at all or not.


## -parameters




### -param TargetUrl [in]

Specifies the storage device or network share to be validated.


### -param ValidationResult [out]

On return, contains a value specifying the result of the device validation. See  the <a href="https://msdn.microsoft.com/DAADC244-D0F5-44F9-9F61-48E6C6EFB91A">FH_DEVICE_VALIDATION_RESULT</a> enumeration for a detailed description of supported device validation results.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\myserver\myshare\").





## -see-also




<a href="https://msdn.microsoft.com/DAADC244-D0F5-44F9-9F61-48E6C6EFB91A">FH_DEVICE_VALIDATION_RESULT</a>



<a href="https://msdn.microsoft.com/BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D">FhReassociation</a>



<a href="https://msdn.microsoft.com/B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588">IFhReassociation</a>
 

 

