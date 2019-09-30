---
UID: NF:fhcfg.IFhConfigMgr.SaveConfiguration
title: IFhConfigMgr::SaveConfiguration (fhcfg.h)
author: windows-sdk-content
description: Saves to disk all the changes that were made in an FhConfigMgr object since the last time that the LoadConfiguration, CreateDefaultConfiguration or SaveConfiguration method was called for the File History configuration files of the current user.
old-location: winprog\ifhconfigmgr_saveconfiguration.htm
tech.root: DevNotes
ms.assetid: 71D6E732-927B-4AA4-9947-6E52B09FF5B8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],SaveConfiguration method, IFhConfigMgr interface [Windows API],SaveConfiguration method, IFhConfigMgr.SaveConfiguration, IFhConfigMgr::SaveConfiguration, SaveConfiguration, SaveConfiguration method [Windows API], SaveConfiguration method [Windows API],FhConfigMgr class, SaveConfiguration method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::SaveConfiguration, winprog.ifhconfigmgr_saveconfiguration
ms.topic: method
f1_keywords: 
 - "fhcfg/IFhConfigMgr.SaveConfiguration"
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
 - IFhConfigMgr.SaveConfiguration
 - FhConfigMgr.SaveConfiguration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhConfigMgr::SaveConfiguration


## -description


Saves to disk all the changes that were made in an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object since the last time that the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">LoadConfiguration</a>, <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">CreateDefaultConfiguration</a> or <b>SaveConfiguration</b> method was called  for the File History configuration files of the current user.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters






## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This method can be called as many times as needed during the lifetime of an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">IFhConfigMgr::CreateDefaultConfiguration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">IFhConfigMgr::LoadConfiguration</a>
 

 

