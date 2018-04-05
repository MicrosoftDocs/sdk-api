---
UID: NF:wuapi.IUpdateInstaller.RunWizard
title: IUpdateInstaller::RunWizard method
author: windows-driver-content
description: Starts a wizard that guides the local user through the steps to install the updates.
old-location: wua\iupdateinstaller_runwizard.htm
old-project: Wua_Sdk
ms.assetid: 006d95ab-45bc-4110-abd9-e39de58b8a4c
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IUpdateInstaller, IUpdateInstaller interface [Windows Update Agent], RunWizard method, IUpdateInstaller::RunWizard, RunWizard method [Windows Update Agent], RunWizard method [Windows Update Agent], IUpdateInstaller interface, RunWizard,IUpdateInstaller.RunWizard, wua.iupdateinstaller_runwizard, wuapi/IUpdateInstaller::RunWizard
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
-	IUpdateInstaller.RunWizard
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller::RunWizard method


## -description


Starts a wizard that guides the local user through the steps to install the updates.


## -parameters




### -param dialogTitle [in, optional]

An optional string value to be displayed in the title bar of the wizard. 

If an empty string value is used, the following text is displayed: Download and Install Updates.


### -param retval [out]

An <a href="https://msdn.microsoft.com/453945d7-11a3-4237-b1c8-928194be558d">IInstallationResult</a> interface that represents the results of an installation operation for each update that is specified in the request.


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
 

 

