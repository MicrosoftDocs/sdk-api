---
UID: NF:wuapi.IInstallationJob.get_AsyncState
title: IInstallationJob::get_AsyncState
author: windows-sdk-content
description: Gets the caller-specific state object that is passed to the IUpdateInstaller.BeginInstall method or to the IUpdateInstaller.BeginUninstall method.
old-location: wua\iinstallationjob_asyncstate.htm
tech.root: Wua_Sdk
ms.assetid: ff3632de-4fb7-4e82-a642-9c9b38f4063c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: AsyncState property [Windows Update Agent], AsyncState property [Windows Update Agent],IInstallationJob interface, IInstallationJob interface [Windows Update Agent],AsyncState property, IInstallationJob.AsyncState, IInstallationJob.get_AsyncState, IInstallationJob::AsyncState, IInstallationJob::get_AsyncState, get_AsyncState, wua.iinstallationjob_asyncstate, wuapi/IInstallationJob::AsyncState, wuapi/IInstallationJob::get_AsyncState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationJob.AsyncState
 - IInstallationJob.get_AsyncState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInstallationJob::get_AsyncState


## -description


Gets the caller-specific state object that is passed to the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> method or to the  <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method.

This property is read-only.


## -parameters


## -remarks



This state object can be used by the caller to identify a particular download or to pass information from the caller to the implementation of the <a href="https://msdn.microsoft.com/a092dbba-57a4-4deb-be05-26cfa29e33aa">IInstallationProgressChangedCallback</a>  interface or the <a href="https://msdn.microsoft.com/930d33e1-e407-4306-acc6-1d64c385a41d">IInstallationCompletedCallback</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a>
 

 

