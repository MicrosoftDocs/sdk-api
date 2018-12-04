---
UID: NF:wuapi.IUpdate.get_UninstallationNotes
title: IUpdate::get_UninstallationNotes
author: windows-sdk-content
description: Gets the uninstallation notes for the update.
old-location: wua\iupdate_uninstallationnotes.htm
tech.root: wua_sdk
ms.assetid: e5a84291-2c50-4ede-b69b-07d5a4226164
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUpdate interface [Windows Update Agent],UninstallationNotes property, IUpdate.UninstallationNotes, IUpdate.get_UninstallationNotes, IUpdate::UninstallationNotes, IUpdate::get_UninstallationNotes, UninstallationNotes property [Windows Update Agent], UninstallationNotes property [Windows Update Agent],IUpdate interface, get_UninstallationNotes, wua.iupdate_uninstallationnotes, wuapi/IUpdate::UninstallationNotes, wuapi/IUpdate::get_UninstallationNotes
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
 - IUpdate.UninstallationNotes
 - IUpdate.get_UninstallationNotes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdate::get_UninstallationNotes


## -description


Gets the uninstallation notes for the update.

This property is read-only.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface  is  created by using the <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is  specified by the <a href="https://msdn.microsoft.com/30ee1836-ea70-4dd1-b531-a7ca32ca940d">UserLocale</a> property. This is the <b>UserLocale</b> property  of the <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="https://msdn.microsoft.com/30ee1836-ea70-4dd1-b531-a7ca32ca940d">UserLocale</a> property of <a href="https://msdn.microsoft.com/c074cbc8-6d1b-41dd-a54c-30f02fca9215">IUpdateSession2</a>, or if the <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface  is not  created by using <a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">IUpdateSession::CreateUpdateSearcher</a>, the information that is returned by  this property is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 

