---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
title: WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA
author: windows-driver-content
description: Retrieves quota information for the user after a connection has been authorized.
old-location: winrm\wsman_plugin_authorize_query_quota.htm
old-project: WinRM
ms.assetid: 426a848c-f549-4a41-b92a-c9451738a014
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WSManPluginAuthzQueryQuota, WSManPluginAuthzQueryQuota callback function [Windows Remote Management], winrm.wsman_plugin_authorize_query_quota, wsman/WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA, wsman/WSManPluginAuthzQueryQuota
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wsman.h
api_name:
-	WSManPluginAuthzQueryQuota
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSMAN_PLUGIN_AUTHORIZE_QUERY_QUOTA callback


## -description


Retrieves quota information for the user after a connection has been authorized. This method will be called only if the configuration specifies that quotas are enabled within the authorization plug-in.

The DLL entry point name for this method must be <b>WSManPluginAuthzQueryQuota</b>.


## -parameters




### -param pluginContext [in]

Specifies the context that was returned by a call to <a href="https://msdn.microsoft.com/b3123f52-880b-4d14-a5a2-77c5924de99d">WSManPluginStartup</a>. This parameter represents a specific application initialization of a WinRM plug-in.


### -param *senderDetails [in]

A pointer  to the <a href="https://msdn.microsoft.com/f68a9f75-6808-4dfa-b40f-061da88ead3c">WSMAN_SENDER_DETAILS</a> structure that specifies the identification information of the user.


### -param flags [in]

Reserved for future use. Must be zero.


## -returns



This callback function does not return a value.




## -remarks



The quota is queried on the first call by a particular user and will not be requeried until after the user record times out due to an idle time-out of activity or until a system-wide configuration period is exceeded.

The plug-in must call the <a href="https://msdn.microsoft.com/611e9be3-75b8-4718-ae10-6ebe38010c7f">WSManPluginAuthzQueryQuotaComplete</a> function to terminate the operation whether or not the plug-in can carry out the request. If successful, the plug-in should give a set of quota information that is relevant for this particular user. If the plug-in fails to process the request for any reason,  an appropriate error should be recorded through the callback method and the error will get propagated back to the client as a Simple Object Access Protocol (SOAP) fault if possible; otherwise, the error will be an empty HTTP 500 status error.



