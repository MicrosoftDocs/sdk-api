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

# IWorkspace2::StartRemoteApplicationEx


## -description


Not supported.

Starts a RemoteApp program with additional options and features.


## -parameters




### -param bstrWorkspaceId [in]

A string that contains the ID of the connection  in which to the start the application.


### -param bstrRequestingAppId [in]

A string that contains the ID of an application to launch on the remote desktop.


### -param bstrRequestingAppFamilyName [in]

A string that contains the family name of the application to launch. 


### -param bLaunchIntoImmersiveClient [in]

<b>VARIANT_TRUE</b> to make the remote application launch as though it were accessed via the web client, using the modern Remote Desktop protocol. <b>VARIANT_FALSE</b> to make the remote application launch using classic Terminal Server methodology.


### -param bstrImmersiveClientActivationContext [in]

A string containing the context for the specific remote desktop client.


### -param psaParams [in]

A pointer to an array of <b>BSTR</b> values that contains  parameters to pass to the workspace runtime.

For RDP connections, this parameter contains two strings:

<ul>
<li>Serialized RDP file</li>
<li>Command line parameters for Remote Desktop Connection client</li>
</ul>

## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>StartRemoteApplicationEx</b> contains a number of new features: launching a 3rd party application when the remote destop first starts, handling multiple remote desktops, and launching with the web-based client UI.




## -see-also




<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

