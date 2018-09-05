---
UID: NF:shappmgr.IShellApp.GetPossibleActions
title: IShellApp::GetPossibleActions
author: windows-sdk-content
description: Gets a bitmask of management actions allowed for an application.
old-location: shell\IShellApp_GetPossibleActions.htm
old-project: shell
ms.assetid: e2cdff59-1339-4d00-9bbc-e34e773da1c2
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetPossibleActions, GetPossibleActions method [Windows Shell], GetPossibleActions method [Windows Shell],IShellApp interface, IShellApp interface [Windows Shell],GetPossibleActions method, IShellApp.GetPossibleActions, IShellApp::GetPossibleActions, inet_IShellApp_GetPossibleActions, shappmgr/IShellApp::GetPossibleActions, shell.IShellApp_GetPossibleActions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellApp.GetPossibleActions
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
---

# IShellApp::GetPossibleActions


## -description


Gets a bitmask of management actions allowed for an application.


## -parameters




### -param pdwActions [out]

Type: <b>DWORD*</b>

A pointer to a variable of type <b>DWORD</b> that returns the bitmask of supported actions. The bit flags are described in <a href="https://msdn.microsoft.com/edfd9b1e-7f4d-4350-9d2c-71f59ca4f7eb">APPACTIONFLAGS</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Of the set of <a href="https://msdn.microsoft.com/edfd9b1e-7f4d-4350-9d2c-71f59ca4f7eb">APPACTIONFLAGS</a> bitmasks, Add/Remove Programs only recognizes APPACTION_INSTALL and APPACTION_ADDLATER.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

