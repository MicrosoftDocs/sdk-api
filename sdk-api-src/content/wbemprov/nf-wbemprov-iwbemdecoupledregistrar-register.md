---
UID: NF:wbemprov.IWbemDecoupledRegistrar.Register
title: IWbemDecoupledRegistrar::Register (wbemprov.h)
description: The IWbemDecoupledRegistrar::Register method registers an object interface with WMI.
helpviewer_keywords: ["IWbemDecoupledRegistrar interface [Windows Management Instrumentation]","Register method","IWbemDecoupledRegistrar.Register","IWbemDecoupledRegistrar::Register","Register","Register method [Windows Management Instrumentation]","Register method [Windows Management Instrumentation]","IWbemDecoupledRegistrar interface","Register method [Windows Management Instrumentation]","WbemDecoupledRegistrar object","WbemDecoupledRegistrar object [Windows Management Instrumentation]","Register method","_hmm_iwbemdecoupledregistrar_register","wbemprov/IWbemDecoupledRegistrar::Register","wmi.iwbemdecoupledregistrar_register"]
old-location: wmi\iwbemdecoupledregistrar_register.htm
tech.root: wmi
ms.assetid: 0592310c-dc1b-45df-bf60-613a58dd69ad
ms.date: 12/05/2018
ms.keywords: IWbemDecoupledRegistrar interface [Windows Management Instrumentation],Register method, IWbemDecoupledRegistrar.Register, IWbemDecoupledRegistrar::Register, Register, Register method [Windows Management Instrumentation], Register method [Windows Management Instrumentation],IWbemDecoupledRegistrar interface, Register method [Windows Management Instrumentation],WbemDecoupledRegistrar object, WbemDecoupledRegistrar object [Windows Management Instrumentation],Register method, _hmm_iwbemdecoupledregistrar_register, wbemprov/IWbemDecoupledRegistrar::Register, wmi.iwbemdecoupledregistrar_register
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemDecoupledRegistrar::Register
 - wbemprov/IWbemDecoupledRegistrar::Register
dev_langs:
 - c++
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
---

# IWbemDecoupledRegistrar::Register


## -description

The 
<b>IWbemDecoupledRegistrar::Register</b> method registers an object interface with WMI.

## -parameters

### -param a_Flags [in]

Reserved for future use.

### -param a_Context [in]

Reserved for future use.

### -param a_User [in]

String identifying the user for this registration.

### -param a_Locale [in]

String identifying the locale for this registration.

### -param a_Scope [in]

Object path representing the binding to a WMI provider registration object in a specified namespace. The scope object path can be <b>NULL</b>, indicating that the provider will support all namespaces.

### -param a_Registration [in]

Name of the provider being registered.

### -param pIUnknown [in]

Pointer to an object for particular registration. This interface will be queried to determine the interface support that the object is capable of servicing.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

