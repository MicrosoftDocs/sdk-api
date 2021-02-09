---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_USER
title: WSMAN_PLUGIN_AUTHORIZE_USER (wsman.h)
description: Authorizes a connection.
helpviewer_keywords: ["WSMAN_PLUGIN_AUTHORIZE_USER","WSMAN_PLUGIN_AUTHORIZE_USER callback","WSMAN_PLUGIN_AUTHORIZE_USER callback function [Windows Remote Management]","winrm.wsman_plugin_authorize_user","wsman/WSMAN_PLUGIN_AUTHORIZE_USER"]
old-location: winrm\wsman_plugin_authorize_user.htm
tech.root: winrm
ms.assetid: 4217c47f-956d-4dde-b679-6f00b0457dcd
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_AUTHORIZE_USER, WSMAN_PLUGIN_AUTHORIZE_USER callback, WSMAN_PLUGIN_AUTHORIZE_USER callback function [Windows Remote Management], winrm.wsman_plugin_authorize_user, wsman/WSMAN_PLUGIN_AUTHORIZE_USER
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSMAN_PLUGIN_AUTHORIZE_USER
 - wsman/WSMAN_PLUGIN_AUTHORIZE_USER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wsman.h
api_name:
 - WSMAN_PLUGIN_AUTHORIZE_USER
---

# WSMAN_PLUGIN_AUTHORIZE_USER callback function


## -description

Authorizes a connection. The plug-in should verify that this user is allowed to perform any operations. If the user is allowed to perform operations, the plug-in must report a success. If the user is not allowed to carry out any type of operation, a failure must be returned.

Every new connection does not need to be authorized. After a user has been authorized to connect, a user record is created to track the activities of the user. While that record exists, all new connections will automatically be authorized. The user record will time-out after a configurable amount of time after no activity is detected.

The DLL entry point name for this method must be <b>WSManPluginAuthzUser</b>.

## -parameters

### -param pluginContext [in]

Specifies the context that was returned by a call to <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a>. This parameter represents a specific application initialization of a WinRM plug-in.

### -param senderDetails [in]

A pointer  to the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_sender_details">WSMAN_SENDER_DETAILS</a> structure that specifies the identification information of the user to be authorized.

### -param flags [in]

Reserved for future use. Must be set to zero.

## -remarks

The plug-in must call <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzusercomplete">WSManPluginAuthzUserComplete</a> to report either that the user was successfully authorized with <b>NO_ERROR</b> or that the user was not authorized with <b>ERROR_ACCESS_DENIED</b>. An <b>ERROR_WSMAN_REDIRECT_REQUIRED</b> error should be reported if an HTTP redirect is required for this user, and the new HTTP URI should be recorded in <i>extendedErrorInformation</i> of the <b>WSManPluginAuthzUserComplete</b> method. All other errors report a failure to the client, but no specific information is reported.
