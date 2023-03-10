---
UID: NF:wsman.WSManPluginAuthzQueryQuotaComplete
title: WSManPluginAuthzQueryQuotaComplete function (wsman.h)
description: Called from the WSManPluginAuthzQueryQuota plug-in entry point and must be called whether or not the plug-in can carry out the request.
helpviewer_keywords: ["WSManPluginAuthzQueryQuotaComplete","WSManPluginAuthzQueryQuotaComplete function [Windows Remote Management]","winrm.wsmanpluginauthzqueryquotacomplete","wsman/WSManPluginAuthzQueryQuotaComplete"]
old-location: winrm\wsmanpluginauthzqueryquotacomplete.htm
tech.root: winrm
ms.assetid: 611e9be3-75b8-4718-ae10-6ebe38010c7f
ms.date: 12/05/2018
ms.keywords: WSManPluginAuthzQueryQuotaComplete, WSManPluginAuthzQueryQuotaComplete function [Windows Remote Management], winrm.wsmanpluginauthzqueryquotacomplete, wsman/WSManPluginAuthzQueryQuotaComplete
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManPluginAuthzQueryQuotaComplete
 - wsman/WSManPluginAuthzQueryQuotaComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManPluginAuthzQueryQuotaComplete
---

# WSManPluginAuthzQueryQuotaComplete function


## -description

Called from the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota">WSManPluginAuthzQueryQuota</a> plug-in entry point and  must be called whether or not the plug-in can carry out the request.

## -parameters

### -param senderDetails [in]

A pointer  to the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_sender_details">WSMAN_SENDER_DETAILS</a> structure that was passed into the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota">WSManPluginAuthzQueryQuota</a> plug-in call.

### -param flags [in]

Reserved for future use. Must be zero.

### -param quota [in, optional]

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_authz_quota">WSMAN_AUTHZ_QUOTA</a> structure that specifies quota information for a specific user.

### -param errorCode [in]

Reports either a successful or failed authorization.   If the authorization is successful, the code  should be <b>ERROR_SUCCESS</b>. If a failure happens for any other reason, an appropriate error code should be used.  Any error from this call will be sent back as a Simple Object Access Protocol (SOAP) fault packet.

### -param extendedErrorInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.

## -returns

The method returns <b>ERROR_SUCCESS</b> if it succeeded; otherwise,  it returns <b>ERROR_INVALID_PARAMETER</b>.  If <b>ERROR_INVALID_PARAMETER</b> is returned, either  the <i>senderDetails</i> parameter was <b>NULL</b> or the <i>flags</i> parameter was not zero.   If the method fails, the default quota is used.

## -remarks

If the <i>quota</i> parameter is <b>null</b> and the <i>errorCode</i> is <b>NO_ERROR</b>, the method returns <b>ERROR_INVALID_PARAMETER</b> and the plug-in returns the default quota information.  If the plug-in is not returning a quota, the authorization plug-in should not specify that quotas are available in the configuration because performance might be affected.