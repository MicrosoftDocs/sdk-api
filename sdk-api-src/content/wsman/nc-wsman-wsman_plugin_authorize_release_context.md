---
UID: NC:wsman.WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT
title: WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT (wsman.h)
description: Releases the context that a plug-in reports from either WSManPluginAuthzUserComplete or WSManPluginAuthzOperationComplete.
helpviewer_keywords: ["WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT","WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT callback","WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT callback function [Windows Remote Management]","winrm.wsman_plugin_authorize_release_context","wsman/WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT"]
old-location: winrm\wsman_plugin_authorize_release_context.htm
tech.root: winrm
ms.assetid: f6cdf6cd-b62a-4678-a36e-a2a14662a9a5
ms.date: 12/05/2018
ms.keywords: WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT, WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT callback, WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT callback function [Windows Remote Management], winrm.wsman_plugin_authorize_release_context, wsman/WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT
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
 - WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT
 - wsman/WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT
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
 - WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT
---

# WSMAN_PLUGIN_AUTHORIZE_RELEASE_CONTEXT callback function


## -description

Releases the context that a plug-in reports from either <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzusercomplete">WSManPluginAuthzUserComplete</a> or <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzoperationcomplete">WSManPluginAuthzOperationComplete</a>.  For a particular user, the context reported for both calls is allowed to be the same, as long as the plug-in infrastructure handles the scenario appropriately.  This method is synchronous, and there are no callbacks that are called as a result.

This method will be called under the following scenarios:
<ul>
<li>After the operation is complete, the <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzoperationcomplete">WSManPluginAuthzOperationComplete</a> context is released.   For some operations, such as get, the context will be released after the response is sent for the get operation.  For more complex operations, such as enumeration, the context will not be released until the enumeration has completed.</li>
<li>When the user record times out due to inactivity,  the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_user">WSManPluginAuthzUser</a> method will be called again the next time a request comes in for that user.</li>
<li>If re-authorization needs to occur, the old context will be released after the new one is acquired.   The old context will always be released regardless of whether the authorization succeeds.</li>
</ul>The DLL entry point name for this method must be <b>WSManPluginAuthzReleaseContext</b>.

## -parameters

### -param userAuthorizationContext [in]

Specifies the context that was returned by either <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzusercomplete">WSManPluginAuthzUserComplete</a> or <a href="/windows/desktop/api/wsman/nf-wsman-wsmanpluginauthzoperationcomplete">WSManPluginAuthzOperationComplete</a>.  If these methods return no context, this method will not be called.