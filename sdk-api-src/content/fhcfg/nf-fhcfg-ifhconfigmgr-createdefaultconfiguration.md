---
UID: NF:fhcfg.IFhConfigMgr.CreateDefaultConfiguration
title: IFhConfigMgr::CreateDefaultConfiguration
author: windows-sdk-content
description: Creates File History configuration files with default settings for the current user and loads them into an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_createdefaultconfiguration.htm
old-project: devnotes
ms.assetid: 70F67D8D-E449-4006-BB14-0E5E9B91D517
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CreateDefaultConfiguration, CreateDefaultConfiguration method [Windows API], CreateDefaultConfiguration method [Windows API],FhConfigMgr class, CreateDefaultConfiguration method [Windows API],IFhConfigMgr interface, FhConfigMgr class [Windows API],CreateDefaultConfiguration method, IFhConfigMgr interface [Windows API],CreateDefaultConfiguration method, IFhConfigMgr.CreateDefaultConfiguration, IFhConfigMgr::CreateDefaultConfiguration, fhcfg/IFhConfigMgr::CreateDefaultConfiguration, winprog.ifhconfigmgr_createdefaultconfiguration
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
 - IFhConfigMgr.CreateDefaultConfiguration
 - FhConfigMgr.CreateDefaultConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhConfigMgr::CreateDefaultConfiguration


## -description


Creates File History configuration files with default settings for the current user and loads them into an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters




### -param OverwriteIfExists [in]

If File History configuration files already exist for the current user and this parameter is set to <b>TRUE</b>, those files are overwritten and all previous settings and policies are reset to default values.

If File History configuration files already exist for the current user and this parameter is set to <b>FALSE</b>, those files are not overwritten and an unsuccessful <b>HRESULT</b> value is returned.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This method or the <a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">LoadConfiguration</a> method must be called before any other <a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a> method can be called.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">IFhConfigMgr::LoadConfiguration</a>



<a href="https://msdn.microsoft.com/71D6E732-927B-4AA4-9947-6E52B09FF5B8">IFhConfigMgr::SaveConfiguration</a>
 

 

