---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI


## -description


Launches an advanced association dialog box through which the user can customize the associations for the application specified in <i>pszAppRegName</i>.


## -parameters




### -param pszAppRegistryName






#### - pszAppRegName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the registered name of the application. This value is only valid if it matches one of the application strings registered under <b>HKCU\Software\RegisteredApplications</b> or under <b>HKLM\Software\RegisteredApplications</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Starting in Windows 10, this does not launch the association dialog box. It displays a dialog to the user informing them that they can change the default programs used to open file extensions in their <b>Settings</b>




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>



<a href="https://msdn.microsoft.com/3a4d6f1d-72c2-4bd0-ad44-1c42a5bf9cb6">IApplicationAssociationRegistrationUI</a>
 

 

