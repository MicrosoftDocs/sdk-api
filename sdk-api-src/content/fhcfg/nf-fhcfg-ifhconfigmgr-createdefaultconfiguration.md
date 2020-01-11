---
UID: NF:fhcfg.IFhConfigMgr.CreateDefaultConfiguration
title: IFhConfigMgr::CreateDefaultConfiguration (fhcfg.h)
description: Creates File History configuration files with default settings for the current user and loads them into an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_createdefaultconfiguration.htm
tech.root: DevNotes
ms.assetid: 70F67D8D-E449-4006-BB14-0E5E9B91D517
ms.date: 12/05/2018
ms.keywords: CreateDefaultConfiguration, CreateDefaultConfiguration method [Windows API], CreateDefaultConfiguration method [Windows API],FhConfigMgr class, CreateDefaultConfiguration method [Windows API],IFhConfigMgr interface, FhConfigMgr class [Windows API],CreateDefaultConfiguration method, IFhConfigMgr interface [Windows API],CreateDefaultConfiguration method, IFhConfigMgr.CreateDefaultConfiguration, IFhConfigMgr::CreateDefaultConfiguration, fhcfg/IFhConfigMgr::CreateDefaultConfiguration, winprog.ifhconfigmgr_createdefaultconfiguration
f1_keywords:
- fhcfg/IFhConfigMgr.CreateDefaultConfiguration
dev_langs:
- c++
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
- IFhConfigMgr.CreateDefaultConfiguration
- FhConfigMgr.CreateDefaultConfiguration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhConfigMgr::CreateDefaultConfiguration


## -description


Creates File History configuration files with default settings for the current user and loads them into an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters




### -param OverwriteIfExists [in]

If File History configuration files already exist for the current user and this parameter is set to <b>TRUE</b>, those files are overwritten and all previous settings and policies are reset to default values.

If File History configuration files already exist for the current user and this parameter is set to <b>FALSE</b>, those files are not overwritten and an unsuccessful <b>HRESULT</b> value is returned.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This method or the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">LoadConfiguration</a> method must be called before any other <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a> method can be called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-loadconfiguration">IFhConfigMgr::LoadConfiguration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-saveconfiguration">IFhConfigMgr::SaveConfiguration</a>
 

 

