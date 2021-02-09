---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
title: WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA (wsman.h)
description: Retrieves quota information for the user after a connection has been authorized.
helpviewer_keywords: ["WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA","WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback","WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback function [Windows Remote Management]","winrm.wsman_plugin_authorize_query_quota","wsman/WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA"]
old-location: winrm\wsman_plugin_authorize_query_quota.htm
tech.root: winrm
ms.assetid: 426a848c-f549-4a41-b92a-c9451738a014
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA, WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback, WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback function [Windows Remote Management], winrm.wsman_plugin_authorize_query_quota, wsman/WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
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
 - WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
 - wsman/WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
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
 - WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
---

# WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback function


## -description

Retrieves quota information for the user after a connection has been authorized. This method will be called only if the configuration specifies that quotas are enabled within the authorization plug-in.

The DLL entry point name for this method must be <b>WSManPluginAuthzQueryQuota</b>.

## -parameters

### -param pluginContext [in]

Specifies the context that was returned by a call to <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_startup">WSManPluginStartup</a>. This parameter represents a specific application initialization of a WinRM plug-in.

### -param senderDetails [in]

A pointer  to the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_sender_details">WSMAN_SENDER_DETAILS</a> structure that specifies the identification information of the user.

### -param flags [in]

Reserved for future use. Must be zero.

## -remarks

The quota is queried on the first call by a particular user and will not be requeried until after the user record times out due to an idle time-out of activity or until a system-wide configuration period is exceeded.

The plug-in must call the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete">WSManPluginAuthzQueryQuotaComplete</a> function to terminate the operation whether or not the plug-in can carry out the request. If successful, the plug-in should give a set of quota information that is relevant for this particular user. If the plug-in fails to process the request for any reason,  an appropriate error should be recorded through the callback method and the error will get propagated back to the client as a Simple Object Access Protocol (SOAP) fault if possible; otherwise, the error will be an empty HTTP 500 status error.
