---
UID: NN:shobjidl_core.IApplicationActivationManager
title: IApplicationActivationManager (shobjidl_core.h)
description: Provides methods which activate Windows Store apps for the Launch, File, and Protocol extensions. You will normally use this interface in debuggers and design tools.
helpviewer_keywords: ["IApplicationActivationManager","IApplicationActivationManager interface [Windows Shell]","IApplicationActivationManager interface [Windows Shell]","described","shell.IApplicationActivationManager","shobjidl_core/IApplicationActivationManager"]
old-location: shell\IApplicationActivationManager.htm
tech.root: shell
ms.assetid: 66C8EDC8-AF05-46d6-B29D-B6EE09DF6709
ms.date: 12/05/2018
ms.keywords: IApplicationActivationManager, IApplicationActivationManager interface [Windows Shell], IApplicationActivationManager interface [Windows Shell],described, shell.IApplicationActivationManager, shobjidl_core/IApplicationActivationManager
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IApplicationActivationManager
 - shobjidl_core/IApplicationActivationManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager
---

# IApplicationActivationManager interface


## -description

Provides methods which activate Windows Store apps for the Launch, File, and Protocol <a href="/previous-versions/windows/apps/hh464906(v=win.10)">extensions</a>. You will normally use this interface in debuggers and design tools.

## -inheritance

The <b>IApplicationActivationManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IApplicationActivationManager</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface yourself. Windows provides an implementation as part of the CApplicationActivationManager class. To get an instance of this class, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the CLSID_ApplicationActivationManager class ID.

<h3><a id="Usage_notes"></a><a id="usage_notes"></a><a id="USAGE_NOTES"></a>Usage notes</h3>
An <b>IApplicationActivationManager</b> object creates a thread in its host process to serve any activated event arguments objects (<a href="/uwp/api/windows.applicationmodel.activation.launchactivatedeventargs">LaunchActivatedEventArgs</a>, <a href="/uwp/api/windows.applicationmodel.activation.fileactivatedeventargs">FileActivatedEventArgs</a>, and <a href="/uwp/api/windows.applicationmodel.activation.protocolactivatedeventargs">ProtocolActivatedEventArgs</a>) that are passed to the app. If the calling process is long-lived, you can create this object in-proc, based on the assumption that the event arguments will exist long enough for the target app to use them. However, if the calling process is spawned only to launch the target app, it should create the <b>IApplicationActivationManager</b> object out-of-process, by using CLSCTX_LOCAL_SERVER. This causes the object to be created in a Dllhost.exe instance that automatically manages the object's lifetime based on outstanding references to the activated event argument objects.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
