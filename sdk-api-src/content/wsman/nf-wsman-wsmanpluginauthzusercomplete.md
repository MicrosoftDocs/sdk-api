---
UID: NF:wsman.WSManPluginAuthzUserComplete
title: WSManPluginAuthzUserComplete function (wsman.h)
author: windows-sdk-content
description: Reports either a successful or failed user connection authorization.
old-location: winrm\wsmanpluginauthzusercomplete.htm
tech.root: winrm
ms.assetid: f8897936-91fa-4b91-a13a-0ef0a52d780c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSManPluginAuthzUserComplete, WSManPluginAuthzUserComplete function [Windows Remote Management], winrm.wsmanpluginauthzusercomplete, wsman/WSManPluginAuthzUserComplete
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
 - WSManPluginAuthzUserComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
---

# WSManPluginAuthzUserComplete function


## -description


Called from the <a href="https://msdn.microsoft.com/4217c47f-956d-4dde-b679-6f00b0457dcd">WSManPluginAuthzUser</a> plug-in entry point and  reports either a successful or failed user connection authorization.


## -parameters




### -param senderDetails [in]

A pointer  to the <a href="https://msdn.microsoft.com/f68a9f75-6808-4dfa-b40f-061da88ead3c">WSMAN_SENDER_DETAILS</a> structure that was passed into the <a href="https://msdn.microsoft.com/4217c47f-956d-4dde-b679-6f00b0457dcd">WSManPluginAuthzUser</a> plug-in call.


### -param flags [in]

Reserved for future use. Must be set to zero.


### -param userAuthorizationContext [in, optional]

Specifies a plug-in defined context that is used to help track user context information. This context can be returned to multiple calls, to this call, or to an operation call.  The plug-in manages reference counting for all calls.  If the user record times out or re-authorization is required, the WinRM infrastructure calls <a href="https://msdn.microsoft.com/f6cdf6cd-b62a-4678-a36e-a2a14662a9a5">WSManPluginAuthzReleaseContext</a>.


### -param impersonationToken [in, optional]

Specifies the identity of the user. This parameter is the  <i>clientToken</i> that was passed into <i>senderDetails</i>. If the plug-in changes the user context, a new impersonation token should be returned.

<div class="alert"><b>Note</b>  This token is released after the operation has been completed.</div>
<div> </div>

### -param userIsAdministrator [in]

Set to <b>TRUE</b> if the user is an administrator. Otherwise, this parameter is <b>FALSE</b>.


### -param errorCode [in]

Reports either a successful or failed authorization.  If the authorization is successful, the code  should be <b>ERROR_SUCCESS</b>.  If the user is not authorized to perform the operation,  the error  should be <b>ERROR_ACCESS_DENIED</b>.  If a failure happens for any other reason, an appropriate error code should be used.  Any error from this call will be sent back as a SOAP fault packet.


### -param extendedErrorInformation [in, optional]

Specifies an XML document that contains any extra error information that needs to be reported to the client. This parameter is ignored if <i>errorCode</i> is <b>NO_ERROR</b>. The user interface language of the thread should be used for localization.


## -returns



The method returns <b>ERROR_SUCCESS</b> if it succeeded; otherwise,  it returns <b>ERROR_INVALID_PARAMETER</b>.  If <b>ERROR_INVALID_PARAMETER</b> is returned, either  the <i>senderDetails</i> parameter was <b>NULL</b> or the <i>flags</i> parameter was not zero.




## -remarks



If the impersonation token passed into <i>senderDetails</i> is not the identity with which the operation should be performed, or if no impersonation token is available and the plug-in specifies a new  identity to carry out the request, the plug-in should return the new <i>impersonationToken</i> that the WSMan infrastructure will use to impersonate the client before calling into the operation plug-in. If an impersonation token is provided in the <i>senderDetails</i> and the plug-in wants to carry out the operation under that identity, the plug-in should copy the impersonation token from the <i>senderDetails</i> into the <i>impersonationToken</i> parameter. If the plug-in wants to carry out the request under the context of the Internet Information Services (IIS) host process, the <i>impersonationToken</i> should be <b>NULL</b>. If the <i>impersonationToken</i> is <b>NULL</b>, the thread will impersonate the process token before calling into the operation plug-in. 

If the <i>userIsAdministrator</i> parameter is set to <b>TRUE</b>, the user is allowed to view and delete shells owned by different users.



