---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_USER
title: WSMAN_PLUGIN_AUTHORIZE_USER (wsman.h)
author: windows-sdk-content
description: Authorizes a connection.
old-location: winrm\wsman_plugin_authorize_user.htm
tech.root: winrm
ms.assetid: 4217c47f-956d-4dde-b679-6f00b0457dcd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_PLUGIN_AUTHORIZE_USER, WSMAN_PLUGIN_AUTHORIZE_USER callback, WSMAN_PLUGIN_AUTHORIZE_USER callback function [Windows Remote Management], winrm.wsman_plugin_authorize_user, wsman/WSMAN_PLUGIN_AUTHORIZE_USER
ms.topic: callback
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_AUTHORIZE_USER
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSMAN_PLUGIN_AUTHORIZE_USER callback function


## -description


Authorizes a connection. The plug-in should verify that this user is allowed to perform any operations. If the user is allowed to perform operations, the plug-in must report a success. If the user is not allowed to carry out any type of operation, a failure must be returned.

Every new connection does not need to be authorized. After a user has been authorized to connect, a user record is created to track the activities of the user. While that record exists, all new connections will automatically be authorized. The user record will time-out after a configurable amount of time after no activity is detected.

The DLL entry point name for this method must be <b>WSManPluginAuthzUser</b>.


## -parameters




### -param pluginContext [in]

Specifies the context that was returned by a call to <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a>. This parameter represents a specific application initialization of a WinRM plug-in.


### -param *senderDetails [in]

A pointer  to the <a href="https://msdn.microsoft.com/f68a9f75-6808-4dfa-b40f-061da88ead3c">WSMAN_SENDER_DETAILS</a> structure that specifies the identification information of the user to be authorized.


### -param flags [in]

Reserved for future use. Must be set to zero.


## -returns



This callback function does not return a value.




## -remarks



The plug-in must call <a href="https://msdn.microsoft.com/f8897936-91fa-4b91-a13a-0ef0a52d780c">WSManPluginAuthzUserComplete</a> to report either that the user was successfully authorized with <b>NO_ERROR</b> or that the user was not authorized with <b>ERROR_ACCESS_DENIED</b>. An <b>ERROR_WSMAN_REDIRECT_REQUIRED</b> error should be reported if an HTTP redirect is required for this user, and the new HTTP URI should be recorded in <i>extendedErrorInformation</i> of the <b>WSManPluginAuthzUserComplete</b> method. All other errors report a failure to the client, but no specific information is reported.



