---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CWbemProviderGlue::FrameworkLoginDLL(LPCWSTR,PLONG)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>FrameworkLoginDLL</b> method is called when the DLL_PROCESS_ATTACH value is sent to DllMain to determine whether the provider server can be loaded.


## -parameters




### -param name

Name of the server that is loaded.


### -param plRefCount






## -returns



The method returns <b>TRUE</b> if the server can be loaded and <b>FALSE</b> if the server cannot be loaded.




## -remarks



The <b>FrameworkLoginDLL</b> method should be called from DllMain when the <i>fdwReason</i> parameter has the value DLL_PROCESS_ATTACH. If <b>FrameworkLoginDLL</b> returns <b>FALSE</b>, the server should return <b>FALSE</b> from DllMain to fail the load.



