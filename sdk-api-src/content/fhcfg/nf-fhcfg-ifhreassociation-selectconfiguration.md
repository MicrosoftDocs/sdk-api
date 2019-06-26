---
UID: NF:fhcfg.IFhReassociation.SelectConfiguration
title: IFhReassociation::SelectConfiguration (fhcfg.h)
author: windows-sdk-content
description: Selects one of the File History configurations discovered on a storage device or network share by the IFhReassociation::ScanTargetForConfigurations method for subsequent reassociation.
old-location: winprog\ifhreassociation_selectconfiguration.htm
tech.root: DevNotes
ms.assetid: 5501F87D-2998-4CB7-B9C8-9EC04F42B22D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FhReassociation class [Windows API],SelectConfiguration method, IFhReassociation interface [Windows API],SelectConfiguration method, IFhReassociation.SelectConfiguration, IFhReassociation::SelectConfiguration, SelectConfiguration, SelectConfiguration method [Windows API], SelectConfiguration method [Windows API],FhReassociation class, SelectConfiguration method [Windows API],IFhReassociation interface, fhcfg/IFhReassociation::SelectConfiguration, winprog.ifhreassociation_selectconfiguration
ms.topic: method
f1_keywords: 
 - "fhcfg/IFhReassociation.SelectConfiguration"
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
 - IFhReassociation.SelectConfiguration
 - FhReassociation.SelectConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhReassociation::SelectConfiguration


## -description


Selects one of the File History configurations discovered on a storage device or network share by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a> method for subsequent reassociation. Actual reassociation is performed by the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a> method.

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -parameters




### -param Index [in]

Zero-based index of a discovered configuration.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

If there is no File History configuration with the specified index, the <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code> error code is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhreassociation">FhReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhreassociation">IFhReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-scantargetforconfigurations">IFhReassociation::ScanTargetForConfigurations</a>
 

 

