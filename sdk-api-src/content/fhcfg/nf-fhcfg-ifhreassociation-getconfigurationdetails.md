---
UID: NF:fhcfg.IFhReassociation.GetConfigurationDetails
title: IFhReassociation::GetConfigurationDetails
author: windows-sdk-content
description: This method enumerates File History configurations that were discovered on a storage device or network share by the IFhReassociation::ScanTargetForConfigurations method and returns additional information about each of the discovered configurations.
old-location: winprog\ifhreassociation_getconfigurationdetails.htm
old-project: devnotes
ms.assetid: 4B5259B7-D845-4CF1-AC33-56DF9D00F2E2
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: FhReassociation class [Windows API],GetConfigurationDetails method, GetConfigurationDetails, GetConfigurationDetails method [Windows API], GetConfigurationDetails method [Windows API],FhReassociation class, GetConfigurationDetails method [Windows API],IFhReassociation interface, IFhReassociation interface [Windows API],GetConfigurationDetails method, IFhReassociation.GetConfigurationDetails, IFhReassociation::GetConfigurationDetails, fhcfg/IFhReassociation::GetConfigurationDetails, winprog.ifhreassociation_getconfigurationdetails
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhReassociation.GetConfigurationDetails
 - FhReassociation.GetConfigurationDetails
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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
 

 

