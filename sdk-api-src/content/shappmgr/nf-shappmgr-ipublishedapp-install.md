---
UID: NF:shappmgr.IPublishedApp.Install
title: IPublishedApp::Install
author: windows-sdk-content
description: Installs an application published by an application publisher. This method is invoked when the user selects Add or Add Later in Add/Remove Programs in Control Panel.
old-location: shell\IPublishedApp_Install.htm
old-project: shell
ms.assetid: 6d8c5720-b48f-4268-810c-c04b14d20d73
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPublishedApp interface [Windows Shell],Install method, IPublishedApp.Install, IPublishedApp::Install, Install, Install method [Windows Shell], Install method [Windows Shell],IPublishedApp interface, inet_IPublishedApp_Install, shappmgr/IPublishedApp::Install, shell.IPublishedApp_Install
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Shappmgr.h
api_name:
 - IPublishedApp.Install
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPublishedApp::Install


## -description


Installs an application published by an application publisher. This method is invoked when the user selects <b>Add</b> or <b>Add Later</b> in <b>Add/Remove Programs</b> in Control Panel.


## -parameters




### -param pstInstall [in]

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that specifies the time the user elected to schedule installation through the <b>Add Later</b> button in <b>Add/Remove Programs</b>. This option is only available if the application supports scheduled installation (compare <a href="https://msdn.microsoft.com/e2cdff59-1339-4d00-9bbc-e34e773da1c2">GetPossibleActions</a>). If this parameter is <b>NULL</b>, the application should be installed immediately.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e2cdff59-1339-4d00-9bbc-e34e773da1c2">GetPossibleActions</a>



<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>
 

 

