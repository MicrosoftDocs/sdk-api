---
UID: NF:fhcfg.IFhConfigMgr.LoadConfiguration
title: IFhConfigMgr::LoadConfiguration
author: windows-sdk-content
description: Loads the File History configuration information for the current user into an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_loadconfiguration.htm
old-project: DevNotes
ms.assetid: 9959AF70-87C2-45E0-A409-959494AF393B
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FhConfigMgr class [Windows API],LoadConfiguration method, IFhConfigMgr interface [Windows API],LoadConfiguration method, IFhConfigMgr.LoadConfiguration, IFhConfigMgr::LoadConfiguration, LoadConfiguration, LoadConfiguration method [Windows API], LoadConfiguration method [Windows API],FhConfigMgr class, LoadConfiguration method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::LoadConfiguration, winprog.ifhconfigmgr_loadconfiguration
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
 - IFhConfigMgr.LoadConfiguration
 - FhConfigMgr.LoadConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhConfigMgr::LoadConfiguration


## -description


Loads the File History configuration information for the current user into an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters






## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



This method or the <a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">IFhConfigMgr::CreateDefaultConfiguration</a> method must be called before any other <a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a> method can be called.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">IFhConfigMgr::CreateDefaultConfiguration</a>



<a href="https://msdn.microsoft.com/71D6E732-927B-4AA4-9947-6E52B09FF5B8">IFhConfigMgr::SaveConfiguration</a>
 

 

