---
UID: NF:wsman.WSManPluginAuthzOperationComplete
title: WSManPluginAuthzOperationComplete function (wsman.h)
description: Reports either a successful or failed authorization for a user operation.
helpviewer_keywords: ["WSManPluginAuthzOperationComplete","WSManPluginAuthzOperationComplete function [Windows Remote Management]","winrm.wsmanpluginauthzoperationcomplete","wsman/WSManPluginAuthzOperationComplete"]
old-location: winrm\wsmanpluginauthzoperationcomplete.htm
tech.root: winrm
ms.assetid: 1b9590ac-45d7-4eed-9477-05500c8bc1ca
ms.date: 12/05/2018
ms.keywords: WSManPluginAuthzOperationComplete, WSManPluginAuthzOperationComplete function [Windows Remote Management], winrm.wsmanpluginauthzoperationcomplete, wsman/WSManPluginAuthzOperationComplete
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
 - WSManPluginAuthzOperationComplete
 - wsman/WSManPluginAuthzOperationComplete
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
 - WSManPluginAuthzOperationComplete
---

# WSManPluginAuthzOperationComplete function


## -description

Called from the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_operation">WSManPluginAuthzOperation</a> plug-in entry point. It reports either a successful or failed authorization for a user operation.

## -parameters

### -param senderDetails [in]

A pointer  to the <a href="/windows/desktop/api/wsman/ns-wsman-wsman_sender_details">WSMAN_SENDER_DETAILS</a> structure that was passed into the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_operation">WSManPluginAuthzOperation</a> plug-in call.

### -param flags [in]

Reserved for future use. Must be zero.

### -param userAuthorizationContext [in, optional]

Specifies a plug-in defined context that is used to help track user context information. This context can be returned to multiple calls, to this call, or to an operation call.  The plug-in manages reference counting for all calls.  If the user record times out or re-authorization is required, the WinRM (WinRM) infrastructure calls <a href="/windows/desktop/api/wsman/nc-wsman-wsman_plugin_authorize_release_context">WSManPluginAuthzReleaseContext</a>.

### -param errorCode [in]

Reports either a successful or failed authorization.  If the authorization is successful, the code  should be <b>ERROR_SUCCESS</b>.  If the user is not authorized to perform the operation,  the error  should be <b>ERROR_ACCESS_DENIED</b>.  If a failure happens for any other reason,  an appropriate error code should be used.  Any error from this call will be sent back as a Simple Object Access Protocol (SOAP) fault packet.

### -param extendedErrorInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.

## -returns

The method returns <b>ERROR_SUCCESS</b> if it succeeded; otherwise,  it returns <b>ERROR_INVALID_PARAMETER</b>.  If <b>ERROR_INVALID_PARAMETER</b> is returned, either  the <i>senderDetails</i> parameter was <b>NULL</b> or the <i>flags</i> parameter was not zero.