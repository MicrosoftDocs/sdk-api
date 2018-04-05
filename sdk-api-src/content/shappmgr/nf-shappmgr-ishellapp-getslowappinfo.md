---
UID: NF:shappmgr.IShellApp.GetSlowAppInfo
title: IShellApp::GetSlowAppInfo method
author: windows-driver-content
description: Returns information to the application that originates from a slow source. This method is not applicable to published applications.
old-location: shell\IShellApp_GetSlowAppInfo.htm
old-project: shell
ms.assetid: 02f8e527-1c3c-4a2e-bf55-4f33c6a7b822
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetSlowAppInfo method [Windows Shell], GetSlowAppInfo method [Windows Shell], IShellApp interface, GetSlowAppInfo,IShellApp.GetSlowAppInfo, IShellApp, IShellApp interface [Windows Shell], GetSlowAppInfo method, IShellApp::GetSlowAppInfo, inet_IShellApp_GetSlowAppInfo, shappmgr/IShellApp::GetSlowAppInfo, shell.IShellApp_GetSlowAppInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shappmgr.h
req.include-header: 
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
req.typenames: PUBAPPINFOFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellApp.GetSlowAppInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IShellApp::GetSlowAppInfo method


## -description


Returns information to the application that originates from a slow source. This method is not applicable to published applications.


## -parameters




### -param psaid [out]

Type: <b>PSLOWAPPINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/e9af8c70-0f03-4f16-bbfb-5e54f7c6c9df">SLOWAPPINFO</a> structure in which to return application information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implementations of <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> should return E_NOTIMPL. This method is used internally by Add/Remove Programs for installed applications.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

