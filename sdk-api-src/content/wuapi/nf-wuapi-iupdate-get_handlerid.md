---
UID: NF:wuapi.IUpdate.get_HandlerID
title: IUpdate::get_HandlerID
author: windows-sdk-content
description: Gets the install handler of the update.
old-location: wua\iupdate_handlerid.htm
old-project: wua_sdk
ms.assetid: af7d4b22-c4e2-4f3d-bef6-5a0cc4f4d5a5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: HandlerID property [Windows Update Agent], HandlerID property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],HandlerID property, IUpdate.HandlerID, IUpdate.get_HandlerID, IUpdate::HandlerID, IUpdate::get_HandlerID, get_HandlerID, wua.iupdate_handlerid, wuapi/IUpdate::HandlerID, wuapi/IUpdate::get_HandlerID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.HandlerID
 - IUpdate.get_HandlerID
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdate::get_HandlerID


## -description


Gets the install handler of the update.

This property is read-only.


## -parameters


## -remarks



The valid values for the <b>HandlerID</b> property include the following:

<ul>
<li>The Command Line Installation Handlerhttp://schemas.microsoft.com/msus/2002/12/UpdateHandlers/CommandLineInstallation

</li>
<li>The Inf Based Installation Handlerhttp://schemas.microsoft.com/msus/2002/12/UpdateHandlers/InfBasedInstallation

</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Cc185688(v=VS.85).aspx">Windows Installer</a> Installation Handlerhttp://schemas.microsoft.com/msus/2002/12/UpdateHandlers/WindowsInstaller

</li>
<li>The Package Installer for Microsoft Windows Operating Systems and Windows Components (update.exe) Installation Handlerhttp://schemas.microsoft.com/msus/2002/12/UpdateHandlers/WindowsPatch

</li>
<li>The Component Based Servicing (CBS) Handlerhttp://schemas.microsoft.com/msus/2002/12/UpdateHandlers/Cbs

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

