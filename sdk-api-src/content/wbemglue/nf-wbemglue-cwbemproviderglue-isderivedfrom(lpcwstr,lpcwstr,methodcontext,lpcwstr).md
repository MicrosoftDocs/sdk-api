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

# CWbemProviderGlue::IsDerivedFrom(LPCWSTR,LPCWSTR,MethodContext,LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/493027c2-e54d-4fad-9e33-98d1ceab8860">CWbemProviderGlue</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>IsDerivedFrom</b> method determines whether one class is derived from another.


## -parameters




### -param pszBaseClassName

Name of base class.


### -param pszDerivedClassName

Name of class to be tested.


### -param pMethodContext

Pointer to the current context. A context must be provided to prevent deadlocks. Either use the context passed into the provider by <a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">Provider::EnumerateInstances</a> or <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a>, or else obtain it from the instance using <a href="https://msdn.microsoft.com/a2033754-4fd0-405f-9ad9-737eb8931016">CInstance::GetMethodContext</a>. This parameter must not be <b>NULL</b>.


### -param pszNamespace

Namespace that contains <i>pszBaseClassName</i> and <i>pszDerivedClassname</i>. If <b>NULL</b>, the default namespace, root\cimv2, is used.


## -returns



The method returns <b>TRUE</b> if the class pointed to by <i>pszDerivedClassName</i> is a subclass of the class pointed to by <i>pszBaseClassName</i> and <b>FALSE</b> if <i>pszDerivedClassName</i> does not derive from <i>pszBaseClassName</i>. If asked if a class is derived from itself, this method returns <b>FALSE</b>.



