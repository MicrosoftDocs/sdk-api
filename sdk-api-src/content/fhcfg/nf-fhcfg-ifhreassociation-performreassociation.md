---
UID: NF:fhcfg.IFhReassociation.PerformReassociation
title: IFhReassociation::PerformReassociation
author: windows-sdk-content
description: This method re-establishes relationship between the current user and the configuration selected previously via the IFhReassociation::SelectConfiguration method and prepares the target device for accepting backup data from the current computer.
old-location: winprog\ifhreassociation_performreassociation.htm
tech.root: DevNotes
ms.assetid: 2E80F25E-2DB6-4522-8F3C-7E6359104CCA
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FhReassociation class [Windows API],PerformReassociation method, IFhReassociation interface [Windows API],PerformReassociation method, IFhReassociation.PerformReassociation, IFhReassociation::PerformReassociation, PerformReassociation, PerformReassociation method [Windows API], PerformReassociation method [Windows API],FhReassociation class, PerformReassociation method [Windows API],IFhReassociation interface, fhcfg/IFhReassociation::PerformReassociation, winprog.ifhreassociation_performreassociation
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFhReassociation.PerformReassociation
 - FhReassociation.PerformReassociation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

