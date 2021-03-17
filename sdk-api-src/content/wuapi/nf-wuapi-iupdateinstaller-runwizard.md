---
UID: NF:wuapi.IUpdateInstaller.RunWizard
title: IUpdateInstaller::RunWizard (wuapi.h)
description: Starts a wizard that guides the local user through the steps to install the updates.
helpviewer_keywords: ["IUpdateInstaller interface [Windows Update Agent]","RunWizard method","IUpdateInstaller.RunWizard","IUpdateInstaller::RunWizard","RunWizard","RunWizard method [Windows Update Agent]","RunWizard method [Windows Update Agent]","IUpdateInstaller interface","wua.iupdateinstaller_runwizard","wuapi/IUpdateInstaller::RunWizard"]
old-location: wua\iupdateinstaller_runwizard.htm
tech.root: wua
ms.assetid: 006d95ab-45bc-4110-abd9-e39de58b8a4c
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller interface [Windows Update Agent],RunWizard method, IUpdateInstaller.RunWizard, IUpdateInstaller::RunWizard, RunWizard, RunWizard method [Windows Update Agent], RunWizard method [Windows Update Agent],IUpdateInstaller interface, wua.iupdateinstaller_runwizard, wuapi/IUpdateInstaller::RunWizard
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
 - IUpdateInstaller::RunWizard
 - wuapi/IUpdateInstaller::RunWizard
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
 - IUpdateInstaller.RunWizard
---

# IUpdateInstaller::RunWizard


## -description

Starts a wizard that guides the local user through the steps to install the updates.

## -parameters

### -param dialogTitle [in, optional]

An optional string value to be displayed in the title bar of the wizard. 

If an empty string value is used, the following text is displayed: Download and Install Updates.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationresult">IInstallationResult</a> interface that represents the results of an installation operation for each update that is specified in the request.

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

This method returns WU_E_NO_UPDATE if the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-get_updates">Updates</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> is not set. This method also returns WU_E_NO_UPDATE if the  <b>Updates</b> property is set to an empty collection.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>