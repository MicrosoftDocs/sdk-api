---
UID: NF:eappapis.EapHostPeerClearConnection
title: EapHostPeerClearConnection function (eappapis.h)
author: windows-sdk-content
description: Clears the authentication session connection.
old-location: eaphost\eaphostpeerclearconnection.htm
tech.root: eaphost
ms.assetid: 1d997e4e-6e7f-47db-9957-9658e54c0bdf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerClearConnection, EapHostPeerClearConnection function [EAPHost], eaphost.eaphostpeerclearconnection, eappapis/EapHostPeerClearConnection
ms.topic: function
f1_keywords: ["eappapis/EapHostPeerClearConnection"]
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerClearConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapHostPeerClearConnection function


## -description


Clears the authentication session connection.  After <b>EapHostPeerClearConnection</b> is called, all states associated with <i>pConnectionId</i> are deleted, and no re-authentication associated with this GUID will be initiated. In addition, all future callbacks to the <a href="https://docs.microsoft.com/windows/desktop/api/eappapis/nc-eappapis-notificationhandler">NotificationHandler</a> callback function (which was passed by the calling supplicant in  a previous call to  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>) are halted. 


## -parameters




### -param pConnectionId [in]

 A pointer to a GUID value that uniquely identifies a logical network interface for a connection to terminate between the supplicant and the EAPHost. This connection ID must have been provided in a previous call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-run-time-functions">EAPHost Supplicant Run-time Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession">EapHostPeerEndSession</a>
 

 

