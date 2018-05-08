---
UID: NF:wuapi.IUpdateInstaller.BeginUninstall
title: IUpdateInstaller::BeginUninstall
author: windows-driver-content
description: Starts an asynchronous uninstallation of the updates.
old-location: wua\iupdateinstaller_beginuninstall.htm
old-project: Wua_Sdk
ms.assetid: 6ff82120-aa8f-4daf-b9f9-e0129fad0a24
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: BeginUninstall, BeginUninstall method [Windows Update Agent], BeginUninstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],BeginUninstall method, IUpdateInstaller.BeginUninstall, IUpdateInstaller::BeginUninstall, wua.iupdateinstaller_beginuninstall, wuapi/IUpdateInstaller::BeginUninstall
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateInstaller.BeginUninstall
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller::BeginUninstall


## -description


Starts an asynchronous uninstallation of the updates.


## -parameters




### -param onProgressChanged [in]

An <a href="https://msdn.microsoft.com/a092dbba-57a4-4deb-be05-26cfa29e33aa">IInstallationProgressChangedCallback</a> interface that is called periodically for uninstallation progress changes before before the uninstallation is complete.


### -param onCompleted [in]

An <a href="https://msdn.microsoft.com/930d33e1-e407-4306-acc6-1d64c385a41d">IInstallationCompletedCallback</a> interface that is called when an installation operation is complete.


### -param state [in]

The caller-specific state that the <a href="https://msdn.microsoft.com/ff3632de-4fb7-4e82-a642-9c9b38f4063c">AsyncState</a> property <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface returns.


### -param retval [out]

An <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface that  contains the properties and methods that are available to an asynchronous uninstall operation that was initiated.


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
<dt><b><b>S_OK</b></b></dt>
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

Call this method only when the <a href="https://msdn.microsoft.com/20875312-f54a-45fc-a0f4-ed17b812dd9e">IsBusy</a> property of the <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface returns <b>VARIANT_FALSE</b>.

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
 

 

