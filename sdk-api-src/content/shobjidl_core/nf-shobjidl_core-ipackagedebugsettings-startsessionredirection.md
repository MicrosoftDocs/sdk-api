---
UID: NF:shobjidl_core.IPackageDebugSettings.StartSessionRedirection
title: IPackageDebugSettings::StartSessionRedirection
author: windows-sdk-content
description: Causes background tasks for the specified package to activate in the specified user session.
old-location: shell\IPackageDebugSettings_StartSessionRedirection.htm
old-project: shell
ms.assetid: a9f40c32-afbe-4f1f-9693-72a757d93a05
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StartSessionRedirection method, IPackageDebugSettings.StartSessionRedirection, IPackageDebugSettings::StartSessionRedirection, StartSessionRedirection, StartSessionRedirection method [Windows Shell], StartSessionRedirection method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StartSessionRedirection, shobjidl_core/IPackageDebugSettings::StartSessionRedirection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.StartSessionRedirection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPackageDebugSettings::StartSessionRedirection


## -description


Causes background tasks for the specified package to activate  in the specified user session.


## -parameters




### -param packageFullName [in]

The package full name.


### -param sessionId [in]

The identifier of the session which background tasks are redirected to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/6edd4f9a-c9e8-45eb-a86b-a04116530aad">StopSessionRedirection</a>
 

 

