---
UID: NF:iscsidsc.SetIScsiIKEInfoW
title: SetIScsiIKEInfoW function (iscsidsc.h)
description: SetIscsiIKEInfo function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections. (Unicode)
helpviewer_keywords: ["SetIScsiIKEInfoW", "SetIscsiIKEInfo", "SetIscsiIKEInfo function [iSCSI Discovery Library API]", "SetIscsiIKEInfoW", "iscsidisc.setiscsiikeinfo", "iscsidsc/SetIscsiIKEInfo", "iscsidsc/SetIscsiIKEInfoW"]
old-location: iscsidisc\setiscsiikeinfo.htm
tech.root: iSCSIDisc
ms.assetid: db020346-45cf-4944-9776-81bb38c7ee6a
ms.date: 12/05/2018
ms.keywords: SetIScsiIKEInfoW, SetIscsiIKEInfo, SetIscsiIKEInfo function [iSCSI Discovery Library API], SetIscsiIKEInfoA, SetIscsiIKEInfoW, iscsidisc.setiscsiikeinfo, iscsidsc/SetIscsiIKEInfo, iscsidsc/SetIscsiIKEInfoA, iscsidsc/SetIscsiIKEInfoW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetIscsiIKEInfoW (Unicode) and SetIscsiIKEInfoA (ANSI)
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
 - SetIScsiIKEInfoW
 - iscsidsc/SetIScsiIKEInfoW
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
 - SetIscsiIKEInfo
 - SetIscsiIKEInfoA
 - SetIscsiIKEInfoW
---

# SetIScsiIKEInfoW function


## -description

The <b>SetIscsiIKEInfo</b> function establishes the IPsec policy and preshared key for the indicated initiator to use when performing iSCSI connections.

## -parameters

### -param InitiatorName [in]

The name of the initiator HBA for which the IPsec policy is established.

### -param InitiatorPortNumber [in]

The port on the initiator HBA with which to associate the key. If this parameter contains a value of <b>ISCSI_ALL_INITIATOR_PORTS</b>, all ports on the initiator are associated with the key.

### -param AuthInfo [in]

A pointer to a <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a> structure that contains the authentication method. Currently, only the IKE_AUTHENTICATION_PRESHARED_KEY_METHOD is supported.

### -param Persist [in]

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-getiscsiikeinfoa">GetIscsiIKEInfo</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-ike_authentication_information">IKE_AUTHENTICATION_INFORMATION</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines SetIScsiIKEInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
