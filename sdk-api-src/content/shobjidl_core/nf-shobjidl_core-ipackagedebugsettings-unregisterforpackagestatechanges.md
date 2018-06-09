---
UID: NF:shobjidl_core.IPackageDebugSettings.UnregisterForPackageStateChanges
title: IPackageDebugSettings::UnregisterForPackageStateChanges
author: windows-sdk-content
description: Stops receiving package state-change notifications associated with a previous call to RegisterForPackageStateChanges.
old-location: shell\IPackageDebugSettings_UnregisterForPackageStateChanges.htm
old-project: shell
ms.assetid: CFCDA0AD-83D5-43DD-A7DD-C121563BF3DB
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],UnregisterForPackageStateChanges method, IPackageDebugSettings.UnregisterForPackageStateChanges, IPackageDebugSettings::UnregisterForPackageStateChanges, UnregisterForPackageStateChanges, UnregisterForPackageStateChanges method [Windows Shell], UnregisterForPackageStateChanges method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_UnregisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::UnregisterForPackageStateChanges
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
 - IPackageDebugSettings.UnregisterForPackageStateChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPackageDebugSettings::UnregisterForPackageStateChanges


## -description


Stops receiving package state-change notifications associated with a previous call to <a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>.


## -parameters




### -param dwCookie






#### - pdwCookie [in]

The notification to cancel. This identifier is returned by a previous call to the  <a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <b>UnregisterForPackageStateChanges</b> to stop receiving package state-change notifications associated with a previous call to the <a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/D0E26154-DADB-499D-A434-8211196E2F5F">RegisterForPackageStateChanges</a>
 

 

