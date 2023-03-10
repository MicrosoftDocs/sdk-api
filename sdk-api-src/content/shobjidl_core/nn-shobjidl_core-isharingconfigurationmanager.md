---
UID: NN:shobjidl_core.ISharingConfigurationManager
title: ISharingConfigurationManager (shobjidl_core.h)
description: Exposes methods that set and retrieve information about a computer's default sharing settings for the Users (C:\Users) or Public (C:\Users\Public) folder. Also exposes a set of methods that allow control of printer sharing.
helpviewer_keywords: ["ISharingConfigurationManager","ISharingConfigurationManager interface [Windows Shell]","ISharingConfigurationManager interface [Windows Shell]","described","_shell_ISharingConfigurationManager","shell.ISharingConfigurationManager","shobjidl_core/ISharingConfigurationManager"]
old-location: shell\ISharingConfigurationManager.htm
tech.root: shell
ms.assetid: 64bf628d-4e9b-42a8-a9cf-04d321645d9a
ms.date: 12/05/2018
ms.keywords: ISharingConfigurationManager, ISharingConfigurationManager interface [Windows Shell], ISharingConfigurationManager interface [Windows Shell],described, _shell_ISharingConfigurationManager, shell.ISharingConfigurationManager, shobjidl_core/ISharingConfigurationManager
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ISharingConfigurationManager
 - shobjidl_core/ISharingConfigurationManager
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
 - ISharingConfigurationManager
---

# ISharingConfigurationManager interface


## -description

Exposes methods that set and retrieve information about a computer's default sharing settings for the <b>Users</b> (<code>C:\Users</code>) or <b>Public</b> (<code>C:\Users\Public</code>) folder. Also exposes a set of methods that allow control of printer sharing.

## -inheritance

The <b>ISharingConfigurationManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISharingConfigurationManager</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is included in the <b>CSharingConfiguration</b> class. Third parties do not provide their own implementation.
