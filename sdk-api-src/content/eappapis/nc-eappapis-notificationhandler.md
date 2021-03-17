---
UID: NC:eappapis.NotificationHandler
title: NotificationHandler (eappapis.h)
description: Notifies the supplicant that there is a change in the Statement of Health (SoH) and re-authentication of a Network Access Protection (NAP) system connection is required.
helpviewer_keywords: ["NotificationHandler","NotificationHandler callback","NotificationHandler callback function [EAPHost]","eaphost.notificationhandler","eappapis/NotificationHandler"]
old-location: eaphost\notificationhandler.htm
tech.root: eaphost
ms.assetid: 7fa12cb4-694a-4db6-9743-5a2cbb995721
ms.date: 12/05/2018
ms.keywords: NotificationHandler, NotificationHandler callback, NotificationHandler callback function [EAPHost], eaphost.notificationhandler, eappapis/NotificationHandler
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NotificationHandler
 - eappapis/NotificationHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - eappapis.h
api_name:
 - NotificationHandler
---

# NotificationHandler callback function


## -description

A callback prototype that notifies the supplicant that there is a change  in the Statement of Health (SoH) and re-authentication of a <a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection</a> (NAP) system connection is required. For the user to receive visual notification of a change in the SoH, the callback must remain in place until after authentication is complete.
<div class="alert"><b>Note</b>  Never cancel the callback while re-authentication is in progress and the network connection is still valid. Never attempt to use any other mechanism to notify the supplicant that the SoH has changed.  </div><div> </div>

## -parameters

### -param connectionId [in]

A GUID provided by the supplicant to EAPHost. This value specifies the logical network connection to re-authenticate.

### -param pContextData [in]

Context data provided to EAPHost by the supplicant. This context data can be used by the supplicant for re-authentication.

## -remarks

A pointer to this callback function must be provided when calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>. The callback may be called by EAPHost at any time prior to calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection">EapHostPeerClearConnection</a>.

## -see-also

[EAPHost Supplicant Callbacks](/windows/win32/eaphost/eap-host-supplicant-callbacks)
