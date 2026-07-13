---
UID: NF:fhcfg.IFhConfigMgr.LoadConfiguration
title: IFhConfigMgr::LoadConfiguration (fhcfg.h)
description: Loads the File History configuration information for the current user into an FhConfigMgr object.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","LoadConfiguration method","IFhConfigMgr interface [Windows API]","LoadConfiguration method","IFhConfigMgr.LoadConfiguration","IFhConfigMgr::LoadConfiguration","LoadConfiguration","LoadConfiguration method [Windows API]","LoadConfiguration method [Windows API]","FhConfigMgr class","LoadConfiguration method [Windows API]","IFhConfigMgr interface","fhcfg/IFhConfigMgr::LoadConfiguration","winprog.ifhconfigmgr_loadconfiguration"]
old-location: winprog\ifhconfigmgr_loadconfiguration.htm
tech.root: winprog
ms.assetid: 9959AF70-87C2-45E0-A409-959494AF393B
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],LoadConfiguration method, IFhConfigMgr interface [Windows API],LoadConfiguration method, IFhConfigMgr.LoadConfiguration, IFhConfigMgr::LoadConfiguration, LoadConfiguration, LoadConfiguration method [Windows API], LoadConfiguration method [Windows API],FhConfigMgr class, LoadConfiguration method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::LoadConfiguration, winprog.ifhconfigmgr_loadconfiguration
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
 - IFhConfigMgr::LoadConfiguration
 - fhcfg/IFhConfigMgr::LoadConfiguration
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
 - IFhConfigMgr.LoadConfiguration
 - FhConfigMgr.LoadConfiguration
---

# IFhConfigMgr::LoadConfiguration


## -description

Loads the File History configuration information for the current user into an <a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

This method or the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">IFhConfigMgr::CreateDefaultConfiguration</a> method must be called before any other <a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a> method can be called.

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-createdefaultconfiguration">IFhConfigMgr::CreateDefaultConfiguration</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-saveconfiguration">IFhConfigMgr::SaveConfiguration</a>
