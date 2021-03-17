---
UID: NF:fhcfg.IFhReassociation.PerformReassociation
title: IFhReassociation::PerformReassociation (fhcfg.h)
description: This method re-establishes relationship between the current user and the configuration selected previously via the IFhReassociation::SelectConfiguration method and prepares the target device for accepting backup data from the current computer.
helpviewer_keywords: ["FhReassociation class [Windows API]","PerformReassociation method","IFhReassociation interface [Windows API]","PerformReassociation method","IFhReassociation.PerformReassociation","IFhReassociation::PerformReassociation","PerformReassociation","PerformReassociation method [Windows API]","PerformReassociation method [Windows API]","FhReassociation class","PerformReassociation method [Windows API]","IFhReassociation interface","fhcfg/IFhReassociation::PerformReassociation","winprog.ifhreassociation_performreassociation"]
old-location: winprog\ifhreassociation_performreassociation.htm
tech.root: winprog
ms.assetid: 2E80F25E-2DB6-4522-8F3C-7E6359104CCA
ms.date: 12/05/2018
ms.keywords: FhReassociation class [Windows API],PerformReassociation method, IFhReassociation interface [Windows API],PerformReassociation method, IFhReassociation.PerformReassociation, IFhReassociation::PerformReassociation, PerformReassociation, PerformReassociation method [Windows API], PerformReassociation method [Windows API],FhReassociation class, PerformReassociation method [Windows API],IFhReassociation interface, fhcfg/IFhReassociation::PerformReassociation, winprog.ifhreassociation_performreassociation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFhReassociation::PerformReassociation
 - fhcfg/IFhReassociation::PerformReassociation
dev_langs:
 - c++
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
---

# IFhReassociation::PerformReassociation


## -description

This method re-establishes relationship between the current user and the configuration selected previously via the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">IFhReassociation::SelectConfiguration</a> method and prepares the target device for accepting backup data from the current computer.

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param OverwriteIfExists [in]

This parameter specifies how to handle the current File History configuration, if it already exists.

If this parameter is set to <b>FALSE</b> and File History is already configured for the current user, this method fails with the <b>FHCFG_E_CONFIG_ALREADY_EXISTS</b> error code and backups continue to be performed to the already configured target device.

If this parameter is set to <b>TRUE</b> and File History is already configured for the current user, the current configuration is replaced with the selected one and future backups after performed to the target device containing the selected configuration.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -see-also

<a href="/windows/desktop/DevNotes/fhreassociation">FhReassociation</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhreassociation">IFhReassociation</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-selectconfiguration">IFhReassociation::SelectConfiguration</a>