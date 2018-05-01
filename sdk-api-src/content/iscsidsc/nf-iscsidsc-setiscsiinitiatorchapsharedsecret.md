---
UID: NF:iscsidsc.SetIScsiInitiatorCHAPSharedSecret
title: SetIScsiInitiatorCHAPSharedSecret function
author: windows-driver-content
description: The SetIscsiInitiatorCHAPSharedSecret function establishes the default Challenge Handshake Authentication Protocol (CHAP) shared secret for all initiators on the computer.
old-location: iscsidisc\setiscsiinitiatorchapsharedsecret.htm
old-project: iSCSIDisc
ms.assetid: 9b7172a5-3a6e-49ae-8f22-77b088eb1048
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: SetIScsiInitiatorCHAPSharedSecret, SetIscsiInitiatorCHAPSharedSecret, SetIscsiInitiatorCHAPSharedSecret function [iSCSI Discovery Library API], iscsidisc.setiscsiinitiatorchapsharedsecret, iscsidsc/SetIscsiInitiatorCHAPSharedSecret
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	SetIscsiInitiatorCHAPSharedSecret
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIScsiInitiatorCHAPSharedSecret function


## -description


The <b>SetIscsiInitiatorCHAPSharedSecret</b> function establishes the default Challenge Handshake Authentication Protocol (CHAP) shared secret for all initiators on the computer.



## -parameters




### -param SharedSecretLength [in]

The size, in bytes, of the shared secret contained by the buffer specified by <i>SharedSecret</i>. The shared secret must be at least 96 bits (12 bytes) for non-IPsec connections, at least 8 bits (1 byte) for IPsec connections, and less than 128 bits (16 bytes) for all connection types.


### -param SharedSecret [in]

The buffer that contains the shared secret.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



When an initiator attempts to log in to a target, the initiator can issue a challenge if mutual CHAP is used. The target must respond to the challenge with the initiator CHAP shared secret.

The <b>SetIscsiInitiatorCHAPSharedSecret</b> function specifies the default CHAP secret that all initiators on the computer use to authenticate a target when performing mutual CHAP. Management software can specify the CHAP secret for the initiator to provide when challenged by the target when the initiator calls the <a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a> or <a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a> function.




## -see-also




<a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a>



<a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a>
 

 

