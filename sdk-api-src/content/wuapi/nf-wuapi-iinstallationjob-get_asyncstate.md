---
UID: NF:wuapi.IInstallationJob.get_AsyncState
title: IInstallationJob::get_AsyncState (wuapi.h)
description: Gets the caller-specific state object that is passed to the IUpdateInstaller.BeginInstall method or to the IUpdateInstaller.BeginUninstall method.
helpviewer_keywords: ["AsyncState property [Windows Update Agent]","AsyncState property [Windows Update Agent]","IInstallationJob interface","IInstallationJob interface [Windows Update Agent]","AsyncState property","IInstallationJob.AsyncState","IInstallationJob.get_AsyncState","IInstallationJob::AsyncState","IInstallationJob::get_AsyncState","get_AsyncState","wua.iinstallationjob_asyncstate","wuapi/IInstallationJob::AsyncState","wuapi/IInstallationJob::get_AsyncState"]
old-location: wua\iinstallationjob_asyncstate.htm
tech.root: wua
ms.assetid: ff3632de-4fb7-4e82-a642-9c9b38f4063c
ms.date: 12/05/2018
ms.keywords: AsyncState property [Windows Update Agent], AsyncState property [Windows Update Agent],IInstallationJob interface, IInstallationJob interface [Windows Update Agent],AsyncState property, IInstallationJob.AsyncState, IInstallationJob.get_AsyncState, IInstallationJob::AsyncState, IInstallationJob::get_AsyncState, get_AsyncState, wua.iinstallationjob_asyncstate, wuapi/IInstallationJob::AsyncState, wuapi/IInstallationJob::get_AsyncState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInstallationJob::get_AsyncState
 - wuapi/IInstallationJob::get_AsyncState
dev_langs:
 - c++
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
---

# IInstallationJob::get_AsyncState


## -description

Gets the caller-specific state object that is passed to the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> method or to the  <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> method.

This property is read-only.

## -parameters

## -remarks

This state object can be used by the caller to identify a particular download or to pass information from the caller to the implementation of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogresschangedcallback">IInstallationProgressChangedCallback</a>  interface or the <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationcompletedcallback">IInstallationCompletedCallback</a> interface.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a>