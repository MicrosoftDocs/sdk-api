---
UID: NF:fsrmscreen.IFsrmFileScreen.get_UserSid
title: IFsrmFileScreen::get_UserSid
author: windows-sdk-content
description: Retrieves the string form of the user's security identifier (SID) that is associated with the file screen.
old-location: fsrm\ifsrmfilescreenbase_usersid.htm
old-project: Fsrm
ms.assetid: 22c20124-1ea7-4e49-845a-da7709e657dd
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFsrmFileScreen interface [File Server Resource Manager],UserSid property, IFsrmFileScreen.UserSid, IFsrmFileScreen.get_UserSid, IFsrmFileScreen::UserSid, IFsrmFileScreen::get_UserSid, UserSid property [File Server Resource Manager], UserSid property [File Server Resource Manager],IFsrmFileScreen interface, fs.ifsrmfilescreenbase_usersid, fsrm.ifsrmfilescreenbase_usersid, fsrmscreen/IFsrmFileScreen::UserSid, fsrmscreen/IFsrmFileScreen::get_UserSid, get_UserSid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreen.UserSid
 - IFsrmFileScreen.get_UserSid
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreen::get_UserSid


## -description


Retrieves the string form of the user's security identifier (SID) that is associated with the file screen.

This property is read-only.


## -parameters


## -remarks



This method always returns the well-known SID, <a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WinNULLSid</a>.




## -see-also




<a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a>



<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>
 

 

