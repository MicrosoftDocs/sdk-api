---
UID: NF:fsrmscreen.IFsrmFileScreen.get_UserAccount
title: IFsrmFileScreen::get_UserAccount
author: windows-sdk-content
description: Retrieves the string form of the user account that is associated with the file screen.
old-location: fsrm\ifsrmfilescreenbase_useraccount.htm
old-project: Fsrm
ms.assetid: 5ed4a98d-eb92-41bc-a193-cdc257ead5c0
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFsrmFileScreen interface [File Server Resource Manager],UserAccount property, IFsrmFileScreen.UserAccount, IFsrmFileScreen.get_UserAccount, IFsrmFileScreen::UserAccount, IFsrmFileScreen::get_UserAccount, UserAccount property [File Server Resource Manager], UserAccount property [File Server Resource Manager],IFsrmFileScreen interface, fs.ifsrmfilescreenbase_useraccount, fsrm.ifsrmfilescreenbase_useraccount, fsrmscreen/IFsrmFileScreen::UserAccount, fsrmscreen/IFsrmFileScreen::get_UserAccount, get_UserAccount
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
 - IFsrmFileScreen.UserAccount
 - IFsrmFileScreen.get_UserAccount
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreen::get_UserAccount


## -description


Retrieves the string form of the user account that is associated with the file screen.

This property is read-only.


## -parameters


## -remarks



This method always returns the string form of the account that corresponds to the well-known SID, <a href="https://msdn.microsoft.com/6f1fa59e-17c0-412b-937b-ddf746ed68bd">WinNULLSid</a>.




## -see-also




<a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a>



<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>
 

 

