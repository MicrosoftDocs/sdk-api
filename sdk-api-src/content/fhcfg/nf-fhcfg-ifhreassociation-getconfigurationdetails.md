---
UID: NF:fhcfg.IFhReassociation.GetConfigurationDetails
title: IFhReassociation::GetConfigurationDetails (fhcfg.h)
author: windows-sdk-content
description: This method enumerates File History configurations that were discovered on a storage device or network share by the IFhReassociation::ScanTargetForConfigurations method and returns additional information about each of the discovered configurations.
old-location: winprog\ifhreassociation_getconfigurationdetails.htm
tech.root: DevNotes
ms.assetid: 4B5259B7-D845-4CF1-AC33-56DF9D00F2E2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FhReassociation class [Windows API],GetConfigurationDetails method, GetConfigurationDetails, GetConfigurationDetails method [Windows API], GetConfigurationDetails method [Windows API],FhReassociation class, GetConfigurationDetails method [Windows API],IFhReassociation interface, IFhReassociation interface [Windows API],GetConfigurationDetails method, IFhReassociation.GetConfigurationDetails, IFhReassociation::GetConfigurationDetails, fhcfg/IFhReassociation::GetConfigurationDetails, winprog.ifhreassociation_getconfigurationdetails
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhReassociation::GetConfigurationDetails


## -description


This method enumerates File History configurations that were discovered on a storage device or network share by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a> method and returns additional information about each of the discovered configurations.


## -parameters




### -param Index [in]

Zero-based index of a discovered configuration.


### -param UserName [out]

On return, contains a pointer to a string allocated with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> containing the name of the user account under which the configuration was last backed up to.


### -param PcName [out]

On return, contains a pointer to a string allocated with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> containing the name of the computer from which the configuration was last backed up.


### -param BackupTime [out]

On return, contains the date and time when the configuration was last backed up.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

If there is no File History configuration with the specified index, the <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code> error code is returned.




## -remarks



The caller is responsible for releasing the memory allocated for <i>UserName</i> and <i>PcName</i> by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> on each of them.

In order to perform reassociation, one of the configurations enumerated by this method must be selected using the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">IFhReassociation::SelectConfiguration</a> method and then the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a> method needs to be called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhreassociation">FhReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhreassociation">IFhReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">IFhReassociation::SelectConfiguration</a>
 

 

