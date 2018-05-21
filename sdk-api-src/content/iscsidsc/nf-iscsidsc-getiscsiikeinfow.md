---
UID: NF:iscsidsc.GetIScsiIKEInfoW
title: GetIScsiIKEInfoW function
author: windows-driver-content
description: GetIscsiIKEInfo function retrieves the IPsec policy and any established pre-shared key values associated with an initiator Host-Bus Adapter (HBA).
old-location: iscsidisc\getiscsiikeinfo.htm
old-project: iSCSIDisc
ms.assetid: 81576452-47bf-4732-a09f-dd1f9e2689c9
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: GetIScsiIKEInfoW, GetIscsiIKEInfo, GetIscsiIKEInfo function [iSCSI Discovery Library API], GetIscsiIKEInfoA, GetIscsiIKEInfoW, iscsidisc.getiscsiikeinfo, iscsidsc/GetIscsiIKEInfo, iscsidsc/GetIscsiIKEInfoA, iscsidsc/GetIscsiIKEInfoW
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
req.unicode-ansi: GetIscsiIKEInfoW (Unicode) and GetIscsiIKEInfoA (ANSI)
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
-	GetIscsiIKEInfo
-	GetIscsiIKEInfoA
-	GetIscsiIKEInfoW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIScsiIKEInfoW function


## -description


The <b>GetIscsiIKEInfo</b> function retrieves the IPsec policy and any established pre-shared key values associated with an initiator Host-Bus Adapter (HBA).


## -parameters




### -param InitiatorName [in, optional]

A string that represents the name of the initiator HBA for which the IPsec policy is established.


### -param InitiatorPortNumber

TBD


### -param Reserved [in]

This value is reserved.


### -param AuthInfo [in]

A pointer to an <a href="https://msdn.microsoft.com/d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0">IKE_AUTHENTICATION_INFORMATION</a> structure that contains data specifying the authentication method. Currently, only the <b>IKE_AUTHENTICATION_PRESHARED_KEY_METHOD</b> is supported.


#### - PortNumber [in]

A <b>ULONG</b> value that represents the port on the initiator HBA with which to associate the key. If this parameter specifies a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.


## -returns



Returns ERROR_SUCCESS if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.



