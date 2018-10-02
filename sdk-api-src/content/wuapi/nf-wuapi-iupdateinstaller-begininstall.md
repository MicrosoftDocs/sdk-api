---
UID: NF:wuapi.IUpdateInstaller.BeginInstall
title: IUpdateInstaller::BeginInstall
author: windows-sdk-content
description: Starts an asynchronous installation of the updates.
old-location: wua\iupdateinstaller_begininstall.htm
tech.root: Wua_Sdk
ms.assetid: 756ad613-bc6b-48fb-a079-c192aa98ccfe
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: BeginInstall, BeginInstall method [Windows Update Agent], BeginInstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],BeginInstall method, IUpdateInstaller.BeginInstall, IUpdateInstaller::BeginInstall, wua.iupdateinstaller_begininstall, wuapi/IUpdateInstaller::BeginInstall
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
 - IUpdateInstaller.BeginInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateInstaller::BeginInstall


## -description


Starts an asynchronous installation of the updates.


## -parameters




### -param onProgressChanged [in]

An <a href="https://msdn.microsoft.com/a092dbba-57a4-4deb-be05-26cfa29e33aa">IInstallationProgressChangedCallback</a> interface that is called periodically for installation progress changes before the installation is complete.


### -param onCompleted [in]

An <a href="https://msdn.microsoft.com/930d33e1-e407-4306-acc6-1d64c385a41d">IInstallationCompletedCallback</a> interface that is called when an installation operation is complete.


### -param state [in]

The caller-specific state that is returned by the <a href="https://msdn.microsoft.com/ff3632de-4fb7-4e82-a642-9c9b38f4063c">AsyncState</a> property of the <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface.


### -param retval [out]

An <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface that contains the properties and methods that are available to an asynchronous installation operation that was initiated.


## -returns



This method returns the following <b>HRESULT</b> values and  other COM or Windows 

error codes.
     

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The asynchronous installation of an update started successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INSTALL_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">
You cannot call this method when the installer is installing or removing an update. 

Only call this method when the <a href="https://msdn.microsoft.com/20875312-f54a-45fc-a0f4-ed17b812dd9e">IsBusy</a> property of the <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface returns <b>VARIANT_FALSE</b>.

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

This method returns WU_E_NO_UPDATE if the <a href="https://msdn.microsoft.com/f56121fd-f8ba-48b5-840b-1a5a751e1a70">Updates</a> property of <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> is not set. This method also returns WU_E_NO_UPDATE if the  <b>Updates</b> property is set to an empty collection.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

