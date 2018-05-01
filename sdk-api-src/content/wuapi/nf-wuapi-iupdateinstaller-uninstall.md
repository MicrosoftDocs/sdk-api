---
UID: NF:wuapi.IUpdateInstaller.Uninstall
title: IUpdateInstaller::Uninstall method
author: windows-driver-content
description: Starts a synchronous uninstallation of the updates.
old-location: wua\iupdateinstaller_uninstall.htm
old-project: Wua_Sdk
ms.assetid: fd00fc89-077e-4897-a7ec-d2e06167b7b0
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IUpdateInstaller, IUpdateInstaller interface [Windows Update Agent], Uninstall method, IUpdateInstaller::Uninstall, Uninstall method [Windows Update Agent], Uninstall method [Windows Update Agent], IUpdateInstaller interface, Uninstall,IUpdateInstaller.Uninstall, wua.iupdateinstaller_uninstall, wuapi/IUpdateInstaller::Uninstall
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
-	IUpdateInstaller.Uninstall
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller::Uninstall method


## -description


Starts a synchronous uninstallation of the updates.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/453945d7-11a3-4237-b1c8-928194be558d">IInstallationResult</a> interface  that represents the results of an uninstallation operation for each update that is specified in a request.


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
An  update uninstalled successfully.

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
There are no updates in a collection.

</td>
</tr>
</table>
 




## -remarks



This method returns WU_E_NO_UPDATE if the <a href="https://msdn.microsoft.com/f56121fd-f8ba-48b5-840b-1a5a751e1a70">Updates</a> property of <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> is not set. This method also returns WU_E_NO_UPDATE if the  <b>Updates</b> property is set to an empty collection.




## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

