---
UID: NF:iscsidsc.GetIScsiIKEInfoW
title: GetIScsiIKEInfoW function (iscsidsc.h)
author: windows-sdk-content
description: GetIscsiIKEInfo function retrieves the IPsec policy and any established pre-shared key values associated with an initiator Host-Bus Adapter (HBA).
old-location: iscsidisc\getiscsiikeinfo.htm
tech.root: iSCSIDisc
ms.assetid: 81576452-47bf-4732-a09f-dd1f9e2689c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIScsiIKEInfoW, GetIscsiIKEInfo, GetIscsiIKEInfo function [iSCSI Discovery Library API], GetIscsiIKEInfoA, GetIscsiIKEInfoW, iscsidisc.getiscsiikeinfo, iscsidsc/GetIscsiIKEInfo, iscsidsc/GetIscsiIKEInfoA, iscsidsc/GetIscsiIKEInfoW
ms.topic: function
f1_keywords: 
 - "iscsidsc/GetIscsiIKEInfo"
dev_langs:
 - c++
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - GetIscsiIKEInfo
 - GetIscsiIKEInfoA
 - GetIscsiIKEInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetIScsiIKEInfoW function


## -description


The <b>GetIscsiIKEInfo</b> function retrieves the IPsec policy and any established pre-shared key values associated with an initiator Host-Bus Adapter (HBA).


## -parameters




### -param InitiatorName [in, optional]

A string that represents the name of the initiator HBA for which the IPsec policy is established.


### -param InitiatorPortNumber [in]

A <b>ULONG</b> value that represents the port on the initiator HBA with which to associate the key. If this parameter specifies a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.


### -param Reserved [in]

This value is reserved.


### -param AuthInfo [in]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a> structure that contains data specifying the authentication method. Currently, only the <b>IKE_AUTHENTICATION_PRESHARED_KEY_METHOD</b> is supported.


## -returns



Returns ERROR_SUCCESS if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.



