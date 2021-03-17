---
UID: NF:iscsidsc.SetIScsiInitiatorRADIUSSharedSecret
title: SetIScsiInitiatorRADIUSSharedSecret function (iscsidsc.h)
description: SetIscsiInitiatorRADIUSSharedSecret function establishes the Remote Authentication Dial-In User Service (RADIUS) shared secret.
helpviewer_keywords: ["SetIScsiInitiatorRADIUSSharedSecret","SetIscsiInitiatorRADIUSSharedSecret","SetIscsiInitiatorRADIUSSharedSecret function [iSCSI Discovery Library API]","iscsidisc.setiscsiinitiatorradiussharedsecret","iscsidsc/SetIscsiInitiatorRADIUSSharedSecret"]
old-location: iscsidisc\setiscsiinitiatorradiussharedsecret.htm
tech.root: iSCSIDisc
ms.assetid: a723256f-adde-4bf2-aab7-152693fa9a21
ms.date: 12/05/2018
ms.keywords: SetIScsiInitiatorRADIUSSharedSecret, SetIscsiInitiatorRADIUSSharedSecret, SetIscsiInitiatorRADIUSSharedSecret function [iSCSI Discovery Library API], iscsidisc.setiscsiinitiatorradiussharedsecret, iscsidsc/SetIscsiInitiatorRADIUSSharedSecret
req.header: iscsidsc.h
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetIScsiInitiatorRADIUSSharedSecret
 - iscsidsc/SetIScsiInitiatorRADIUSSharedSecret
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - SetIscsiInitiatorRADIUSSharedSecret
---

# SetIScsiInitiatorRADIUSSharedSecret function


## -description

The <b>SetIscsiInitiatorRADIUSSharedSecret</b> function establishes the Remote Authentication Dial-In User Service (RADIUS) shared secret.

## -parameters

### -param SharedSecretLength [in]

A <b>ULONG</b> value that represents the size, in bytes, of the shared secret contained by the buffer specified by SharedSecret. The shared secret must be at least 22 bytes, and less than, or equal to, 26 bytes in size.

### -param SharedSecret [in]

A string that specifies the buffer containing the shared secret.

## -returns

Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.

## -remarks

When an initiator attempts to log in to a target, the initiator can use the RADIUS server for authentication, or to authenticate a target. During this process the initiator uses the <i>SharedSecret</i> to communicate with the RADIUS server.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-loginiscsitargeta">LoginIscsiTarget</a>