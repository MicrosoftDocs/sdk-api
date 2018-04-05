---
UID: NF:fhcfg.IFhReassociation.SelectConfiguration
title: IFhReassociation::SelectConfiguration method
author: windows-driver-content
description: Selects one of the File History configurations discovered on a storage device or network share by the IFhReassociation::ScanTargetForConfigurations method for subsequent reassociation.
old-location: winprog\ifhreassociation_selectconfiguration.htm
old-project: DevNotes
ms.assetid: 5501F87D-2998-4CB7-B9C8-9EC04F42B22D
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FhReassociation class [Windows API], SelectConfiguration method, IFhReassociation, IFhReassociation interface [Windows API], SelectConfiguration method, IFhReassociation::SelectConfiguration, SelectConfiguration method [Windows API], SelectConfiguration method [Windows API], FhReassociation class, SelectConfiguration method [Windows API], IFhReassociation interface, SelectConfiguration,IFhReassociation.SelectConfiguration, fhcfg/IFhReassociation::SelectConfiguration, winprog.ifhreassociation_selectconfiguration
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
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fhcfg.h
api_name:
-	IFhReassociation.SelectConfiguration
-	FhReassociation.SelectConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhReassociation::SelectConfiguration method


## -description


Selects one of the File History configurations discovered on a storage device or network share by the <a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a> method for subsequent reassociation. Actual reassociation is performed by the <a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a> method.


## -parameters




### -param Index [in]

Zero-based index of a discovered configuration.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

If there is no File History configuration with the specified index, the <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code> error code is returned.




## -see-also




<a href="https://msdn.microsoft.com/BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D">FhReassociation</a>



<a href="https://msdn.microsoft.com/B1CBD7DD-5B4D-4B3E-BE7D-B6497ABFB588">IFhReassociation</a>



<a href="https://msdn.microsoft.com/2E80F25E-2DB6-4522-8F3C-7E6359104CCA">IFhReassociation::PerformReassociation</a>



<a href="https://msdn.microsoft.com/E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D">IFhReassociation::ScanTargetForConfigurations</a>
 

 

