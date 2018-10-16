---
UID: NF:shappmgr.IShellApp.IsInstalled
title: IShellApp::IsInstalled
author: windows-sdk-content
description: Gets a value indicating whether a specified application is currently installed.
old-location: shell\IShellApp_IsInstalled.htm
tech.root: shell
ms.assetid: 338ba632-5749-4850-b982-2247f0d0dcc5
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IShellApp interface [Windows Shell],IsInstalled method, IShellApp.IsInstalled, IShellApp::IsInstalled, IsInstalled, IsInstalled method [Windows Shell], IsInstalled method [Windows Shell],IShellApp interface, inet_IShellApp_IsInstalled, shappmgr/IShellApp::IsInstalled, shell.IShellApp_IsInstalled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellApp.IsInstalled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellApp::IsInstalled


## -description


Gets a value indicating whether a specified application is currently installed.
		


## -parameters






## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
The application is installed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application is not installed.

</td>
</tr>
</table>
 




## -remarks



Application publishers should determine if the application is currently installed and return S_OK if so, or S_FALSE if not.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>



<a href="https://msdn.microsoft.com/2f56744c-a10e-423f-8b8f-c3257e560310">IShellApp</a>
 

 

