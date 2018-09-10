---
UID: NF:wbemprov.IWbemDecoupledRegistrar.Register
title: IWbemDecoupledRegistrar::Register
author: windows-sdk-content
description: The IWbemDecoupledRegistrar::Register method registers an object interface with WMI.
old-location: wmi\iwbemdecoupledregistrar_register.htm
tech.root: WmiSdk
ms.assetid: 0592310c-dc1b-45df-bf60-613a58dd69ad
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemDecoupledRegistrar interface [Windows Management Instrumentation],Register method, IWbemDecoupledRegistrar.Register, IWbemDecoupledRegistrar::Register, Register, Register method [Windows Management Instrumentation], Register method [Windows Management Instrumentation],IWbemDecoupledRegistrar interface, Register method [Windows Management Instrumentation],WbemDecoupledRegistrar object, WbemDecoupledRegistrar object [Windows Management Instrumentation],Register method, _hmm_iwbemdecoupledregistrar_register, wbemprov/IWbemDecoupledRegistrar::Register, wmi.iwbemdecoupledregistrar_register
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemprov.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmidcprv.dll
api_name:
 - IWbemDecoupledRegistrar.Register
 - WbemDecoupledRegistrar.Register
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemDecoupledRegistrar::Register


## -description


The 
<b>IWbemDecoupledRegistrar::Register</b> method registers an object interface with WMI.


## -parameters




### -param a_Flags

TBD


### -param a_Context

TBD


### -param a_User

TBD


### -param a_Locale

TBD


### -param a_Scope

TBD


### -param a_Registration

TBD


### -param pIUnknown

TBD




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



