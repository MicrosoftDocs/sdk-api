---
UID: NF:iscsidsc.GetIScsiIKEInfoA
title: GetIScsiIKEInfoA function (iscsidsc.h)
description: GetIscsiIKEInfo function retrieves the IPsec policy and any established pre-shared key values associated with an initiator Host-Bus Adapter (HBA). (ANSI)
helpviewer_keywords: ["GetIScsiIKEInfoA", "GetIscsiIKEInfoA", "iscsidsc/GetIscsiIKEInfoA"]
old-location: iscsidisc\getiscsiikeinfo.htm
tech.root: iSCSIDisc
ms.assetid: 81576452-47bf-4732-a09f-dd1f9e2689c9
ms.date: 12/05/2018
ms.keywords: GetIScsiIKEInfoA, GetIscsiIKEInfo, GetIscsiIKEInfo function [iSCSI Discovery Library API], GetIscsiIKEInfoA, GetIscsiIKEInfoW, iscsidisc.getiscsiikeinfo, iscsidsc/GetIscsiIKEInfo, iscsidsc/GetIscsiIKEInfoA, iscsidsc/GetIscsiIKEInfoW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIScsiIKEInfoA
 - iscsidsc/GetIScsiIKEInfoA
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
 - GetIscsiIKEInfo
 - GetIscsiIKEInfoA
 - GetIscsiIKEInfoW
---

# GetIScsiIKEInfoA function


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

A pointer to an <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a> structure that contains data specifying the authentication method. Currently, only the <b>IKE_AUTHENTICATION_PRESHARED_KEY_METHOD</b> is supported.

## -returns

Returns ERROR_SUCCESS if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.

## -remarks

> [!NOTE]
> The iscsidsc.h header defines GetIScsiIKEInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
