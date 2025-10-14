---
UID: NF:wuapi.IUpdateInstaller.BeginUninstall
title: IUpdateInstaller::BeginUninstall (wuapi.h)
description: Starts an asynchronous uninstallation of the updates.
helpviewer_keywords: ["BeginUninstall","BeginUninstall method [Windows Update Agent]","BeginUninstall method [Windows Update Agent]","IUpdateInstaller interface","IUpdateInstaller interface [Windows Update Agent]","BeginUninstall method","IUpdateInstaller.BeginUninstall","IUpdateInstaller::BeginUninstall","wua.iupdateinstaller_beginuninstall","wuapi/IUpdateInstaller::BeginUninstall"]
old-location: wua\iupdateinstaller_beginuninstall.htm
tech.root: wua
ms.assetid: 6ff82120-aa8f-4daf-b9f9-e0129fad0a24
ms.date: 12/05/2018
ms.keywords: BeginUninstall, BeginUninstall method [Windows Update Agent], BeginUninstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],BeginUninstall method, IUpdateInstaller.BeginUninstall, IUpdateInstaller::BeginUninstall, wua.iupdateinstaller_beginuninstall, wuapi/IUpdateInstaller::BeginUninstall
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
 - IUpdateInstaller::BeginUninstall
 - wuapi/IUpdateInstaller::BeginUninstall
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
 - IUpdateInstaller.BeginUninstall
---

# IUpdateInstaller::BeginUninstall


## -description

Starts an asynchronous uninstallation of the updates.

## -parameters

### -param onProgressChanged [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogresschangedcallback">IInstallationProgressChangedCallback</a> interface that is called periodically for uninstallation progress changes before the uninstallation is complete.

### -param onCompleted [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationcompletedcallback">IInstallationCompletedCallback</a> interface that is called when an installation operation is complete.

### -param state [in]

The caller-specific state that the <a href="/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-get_asyncstate">AsyncState</a> property <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface returns.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface that  contains the properties and methods that are available to an asynchronous uninstall operation that was initiated.

## -returns

This method returns the following <b>HRESULT</b> values and other COM or Windows 

error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous removal of an update started successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INSTALL_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
Do not call this method when the installer is installing or removing an update. 

Call this method only when the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-get_isbusy">IsBusy</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> interface returns <b>VARIANT_FALSE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NO_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Windows Update Agent (WUA) does not have updates in the collection.

</td>
</tr>
</table>

## -remarks

  If you call this method from a scripting language, set the <i>onProgressChanged</i> parameter to the identifier of  an Automation object with a dispatch identifier (DSIPID) of zero (0) that implements the callback routine. Do the same thing for the <i>onCompleted</i> parameter.

This method returns WU_E_NO_UPDATE if the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-get_updates">Updates</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> is not set. This method also returns WU_E_NO_UPDATE if the  <b>Updates</b> property is set to an empty collection.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>