---
UID: NF:wsman.WSManPluginAuthzOperationComplete
title: WSManPluginAuthzOperationComplete function
author: windows-sdk-content
description: Reports either a successful or failed authorization for a user operation.
old-location: winrm\wsmanpluginauthzoperationcomplete.htm
tech.root: winrm
ms.assetid: 1b9590ac-45d7-4eed-9477-05500c8bc1ca
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: WSManPluginAuthzOperationComplete, WSManPluginAuthzOperationComplete function [Windows Remote Management], winrm.wsmanpluginauthzoperationcomplete, wsman/WSManPluginAuthzOperationComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManPluginAuthzOperationComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
---

# WSManPluginAuthzOperationComplete function


## -description


Called from the <a href="https://msdn.microsoft.com/28fbd8db-557d-487b-8cf7-c550fe0826f7">WSManPluginAuthzOperation</a> plug-in entry point. It reports either a successful or failed authorization for a user operation.


## -parameters




### -param senderDetails [in]

A pointer  to the <a href="https://msdn.microsoft.com/f68a9f75-6808-4dfa-b40f-061da88ead3c">WSMAN_SENDER_DETAILS</a> structure that was passed into the <a href="https://msdn.microsoft.com/28fbd8db-557d-487b-8cf7-c550fe0826f7">WSManPluginAuthzOperation</a> plug-in call.


### -param flags [in]

Reserved for future use. Must be zero.


### -param userAuthorizationContext [in, optional]

Specifies a plug-in defined context that is used to help track user context information. This context can be returned to multiple calls, to this call, or to an operation call.  The plug-in manages reference counting for all calls.  If the user record times out or re-authorization is required, the WinRM (WinRM) infrastructure calls <a href="https://msdn.microsoft.com/f6cdf6cd-b62a-4678-a36e-a2a14662a9a5">WSManPluginAuthzReleaseContext</a>.


### -param errorCode [in]

Reports either a successful or failed authorization.  If the authorization is successful, the code  should be <b>ERROR_SUCCESS</b>.  If the user is not authorized to perform the operation,  the error  should be <b>ERROR_ACCESS_DENIED</b>.  If a failure happens for any other reason,  an appropriate error code should be used.  Any error from this call will be sent back as a Simple Object Access Protocol (SOAP) fault packet.


### -param extendedErrorInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.


## -returns



The method returns <b>ERROR_SUCCESS</b> if it succeeded; otherwise,  it returns <b>ERROR_INVALID_PARAMETER</b>.  If <b>ERROR_INVALID_PARAMETER</b> is returned, either  the <i>senderDetails</i> parameter was <b>NULL</b> or the <i>flags</i> parameter was not zero.



