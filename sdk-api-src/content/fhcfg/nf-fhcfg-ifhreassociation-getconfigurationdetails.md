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

# IFhReassociation::GetConfigurationDetails


## -description


This method enumerates File History configurations that were discovered on a storage device or network share by the <a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a> method and returns additional information about each of the discovered configurations.


## -parameters




### -param Index [in]

Zero-based index of a discovered configuration.


### -param UserName [out]

On return, contains a pointer to a string allocated with <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> containing the name of the user account under which the configuration was last backed up to.


### -param PcName [out]

On return, contains a pointer to a string allocated with <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> containing the name of the computer from which the configuration was last backed up.


### -param BackupTime [out]

On return, contains the date and time when the configuration was last backed up.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

If there is no File History configuration with the specified index, the <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code> error code is returned.




## -remarks



The caller is responsible for releasing the memory allocated for <i>UserName</i> and <i>PcName</i> by calling <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> on each of them.

In order to perform reassociation, one of the configurations enumerated by this method must be selected using the <a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">IFhReassociation::SelectConfiguration</a> method and then the <a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a> method needs to be called.




## -see-also




<a href="https://msdn.microsoft.com/BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D">FhReassociation</a>



<a href="https://msdn.microsoft.com/B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588">IFhReassociation</a>



<a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a>



<a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a>



<a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">IFhReassociation::SelectConfiguration</a>
 

 

