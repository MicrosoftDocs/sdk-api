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

# IFhReassociation::PerformReassociation


## -description


This method re-establishes relationship between the current user and the configuration selected previously via the <a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">IFhReassociation::SelectConfiguration</a> method and prepares the target device for accepting backup data from the current computer.


## -parameters




### -param OverwriteIfExists [in]

This parameter specifies how to handle the current File History configuration, if it already exists.

If this parameter is set to <b>FALSE</b> and File History is already configured for the current user, this method fails with the <b>FHCFG_E_CONFIG_ALREADY_EXISTS</b> error code and backups continue to be performed to the already configured target device.

If this parameter is set to <b>TRUE</b> and File History is already configured for the current user, the current configuration is replaced with the selected one and future backups after performed to the target device containing the selected configuration.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -see-also




<a href="https://msdn.microsoft.com/BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D">FhReassociation</a>



<a href="https://msdn.microsoft.com/B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588">IFhReassociation</a>



<a href="https://msdn.microsoft.com/5501F87D-2998-4CB7-B9C8-9EC04F42B22D">IFhReassociation::SelectConfiguration</a>
 

 

