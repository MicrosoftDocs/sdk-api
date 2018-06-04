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

# IWbemDecoupledRegistrar::Register


## -description


The 
<b>IWbemDecoupledRegistrar::Register</b> method registers an object interface with WMI.


## -parameters




### -param a_Flags




### -param a_Context




### -param a_User




### -param a_Locale




### -param a_Scope




### -param a_Registration




### -param pIUnknown






#### - lFlags [in]

Reserved for future use.


#### - pContext [in]

Reserved for future use.


#### - pUnknown [in]

Pointer to an object for particular registration. This interface will be queried to determine the interface support that the object is capable of servicing.


#### - strLocal [in]

String identifying the locale for this registration.


#### - strRegistration [in]

Name of the provider being registered.


#### - strScope [in]

Object path representing the binding to a WMI provider registration object in a specified namespace. The scope object path can be <b>NULL</b>, indicating that the provider will support all namespaces.


#### - strUser [in]

String identifying the user for this registration.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.



