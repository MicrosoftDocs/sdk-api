---
UID: NF:iscsidsc.SetIScsiInitiatorRADIUSSharedSecret
title: SetIScsiInitiatorRADIUSSharedSecret function
author: windows-sdk-content
description: SetIscsiInitiatorRADIUSSharedSecret function establishes the Remote Authentication Dial-In User Service (RADIUS) shared secret.
old-location: iscsidisc\setiscsiinitiatorradiussharedsecret.htm
old-project: iSCSIDisc
ms.assetid: a723256f-adde-4bf2-aab7-152693fa9a21
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetIScsiInitiatorRADIUSSharedSecret, SetIscsiInitiatorRADIUSSharedSecret, SetIscsiInitiatorRADIUSSharedSecret function [iSCSI Discovery Library API], iscsidisc.setiscsiinitiatorradiussharedsecret, iscsidsc/SetIscsiInitiatorRADIUSSharedSecret
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - SetIscsiInitiatorRADIUSSharedSecret
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a>
 

 

