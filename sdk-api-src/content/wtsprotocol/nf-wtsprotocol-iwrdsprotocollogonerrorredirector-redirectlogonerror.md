---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.RedirectLogonError
title: IWRdsProtocolLogonErrorRedirector::RedirectLogonError
author: windows-sdk-content
description: Queries the protocol for the action to take in response to a logon error.
old-location: termserv\iwrdsprotocollogonerrorredirector_redirectlogonerror.htm
old-project: termserv
ms.assetid: 86c919e9-2c45-45dd-8eee-7b50efb00cbb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectLogonError method, IWRdsProtocolLogonErrorRedirector.RedirectLogonError, IWRdsProtocolLogonErrorRedirector::RedirectLogonError, RedirectLogonError, RedirectLogonError method [Remote Desktop Services], RedirectLogonError method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, STATUS_ACCOUNT_DISABLED, STATUS_ACCOUNT_RESTRICTION, STATUS_BAD_VALIDATION_CLASS, STATUS_INVALID_LOGON_HOURS, STATUS_INVALID_WORKSTATION, STATUS_LOGON_FAILURE, STATUS_NO_LOGON_SERVERS, STATUS_NO_SUCH_PACKAGE, STATUS_PASSWORD_EXPIRED, STATUS_QUOTA_EXCEEDED, termserv.iwrdsprotocollogonerrorredirector_redirectlogonerror, wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectLogonError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLogonErrorRedirector.RedirectLogonError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolLogonErrorRedirector::RedirectLogonError


## -description


Queries the protocol for the action to take in response to a logon error. The <a href="https://msdn.microsoft.com/f1f6caec-6e26-4508-b19d-ac0e12758b28">RedirectStatus</a> method is called by the Remote Desktop Services service  to query the protocol for the action to take in response to a logon error.


## -parameters




### -param ntsStatus [in]

An integer that contains information about the logon failure. This can be one of the following values.



#### STATUS_QUOTA_EXCEEDED

The memory quota is insufficient to allocate the output buffer returned by the authentication package.



#### STATUS_ACCOUNT_RESTRICTION

The user account and password are legitimate, but the user account has a restriction that prevents logon at this time. For more information, see the <i>ntsSubstatus</i> parameter.



#### STATUS_BAD_VALIDATION_CLASS

The authentication information provided is not recognized by the authentication package.



#### STATUS_LOGON_FAILURE

The logon attempt failed. The reason for the failure is not specified, but typical reasons include misspelled user names and misspelled passwords.



#### STATUS_NO_LOGON_SERVERS

No domain controllers are available to service the authentication request.



#### STATUS_NO_SUCH_PACKAGE

The specified authentication package is not recognized by the LSA.


### -param ntsSubstatus [in]

An integer that contains information about why a logon attempt failed. This value is set only if the account information of the user is valid and the logon is rejected. This can contain one of the following values.



#### STATUS_INVALID_LOGON_HOURS

The user account has time restrictions and cannot be used to log on at this time.



#### STATUS_INVALID_WORKSTATION

The user account has workstation restrictions and cannot be used to log on from the current workstation.



#### STATUS_PASSWORD_EXPIRED

The user account password has expired.



#### STATUS_ACCOUNT_DISABLED

The user account is currently disabled and cannot be used to log on.


### -param pszCaption [in]

A pointer to a string that contains the message box caption.


### -param pszMessage [in]

A pointer to a string that contains the message.


### -param uType [in]

An integer that contains the message box type. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a> function.


### -param pResponse [out]

A pointer to a <a href="https://msdn.microsoft.com/67ed8d6f-641c-4739-911c-e61379e14048">WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that specifies to the Remote Desktop Services service the preferred response to the logon error.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a>
 

 

