---
UID: NF:comadmin.ICOMAdminCatalog.InstallEventClass
title: ICOMAdminCatalog::InstallEventClass (comadmin.h)
description: Installs event classes from a file into a COM+ application.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","InstallEventClass method","ICOMAdminCatalog.InstallEventClass","ICOMAdminCatalog::InstallEventClass","InstallEventClass","InstallEventClass method [COM+]","InstallEventClass method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_InstallEventClass","comadmin/ICOMAdminCatalog::InstallEventClass","cos.icomadmincatalog_installeventclass"]
old-location: cos\icomadmincatalog_installeventclass.htm
tech.root: cos
ms.assetid: 8e9f7c79-076e-46dc-bce0-389c5309e6fa
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],InstallEventClass method, ICOMAdminCatalog.InstallEventClass, ICOMAdminCatalog::InstallEventClass, InstallEventClass, InstallEventClass method [COM+], InstallEventClass method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_InstallEventClass, comadmin/ICOMAdminCatalog::InstallEventClass, cos.icomadmincatalog_installeventclass
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICOMAdminCatalog::InstallEventClass
 - comadmin/ICOMAdminCatalog::InstallEventClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.InstallEventClass
---

# ICOMAdminCatalog::InstallEventClass


## -description

Installs event classes from a file into a COM+ application.

## -parameters

### -param bstrApplIdOrName [in]

The GUID or name of the application.

### -param bstrDLL [in]

The file name of the DLL containing the event classes to be installed.

### -param bstrTLB [in]

The name of an external type library file. If the type library file is embedded in the DLL, pass in an empty string for this parameter.

### -param bstrPSDLL [in]

The name of the proxy-stub DLL file. If there is no proxy-stub DLL associated with the event class, pass in an empty string for this parameter.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

Use <b>InstallEventClass</b> to install event classes from a DLL holding dummy implementations of the event classes. The requirements are a self-registering DLL, a type library describing the interfaces implemented by the event classes, and each event class having a CLSID and a ProgID.

The dummy implementation of the interface exposed by an event class never actually runs; it exists only to register the event class. Instead, when the event class is created by the publisher, an implementation is provided by the Events system to send the event to subscribers.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>