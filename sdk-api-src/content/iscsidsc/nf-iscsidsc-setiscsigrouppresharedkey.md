---
UID: NF:iscsidsc.SetIScsiGroupPresharedKey
title: SetIScsiGroupPresharedKey function (iscsidsc.h)
description: SetIscsiGroupPresharedKey function establishes the default group preshared key for all initiators on the computer.
helpviewer_keywords: ["SetIScsiGroupPresharedKey","SetIscsiGroupPresharedKey","SetIscsiGroupPresharedKey function [iSCSI Discovery Library API]","iscsidisc.setiscsigrouppresharedkey","iscsidsc/SetIscsiGroupPresharedKey"]
old-location: iscsidisc\setiscsigrouppresharedkey.htm
tech.root: iSCSIDisc
ms.assetid: 344d0a88-64e9-45a3-a789-6733b85e9c2d
ms.date: 12/05/2018
ms.keywords: SetIScsiGroupPresharedKey, SetIscsiGroupPresharedKey, SetIscsiGroupPresharedKey function [iSCSI Discovery Library API], iscsidisc.setiscsigrouppresharedkey, iscsidsc/SetIscsiGroupPresharedKey
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
 - SetIScsiGroupPresharedKey
 - iscsidsc/SetIScsiGroupPresharedKey
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
 - SetIscsiGroupPresharedKey
---

# SetIScsiGroupPresharedKey function


## -description

The <b>SetIscsiGroupPresharedKey</b> function establishes the default group preshared key for all initiators on the computer.

## -parameters

### -param KeyLength [in]

The size, in bytes, of the preshared key.

### -param Key [in]

The buffer that contains the preshared key.

### -param Persist

If <b>true</b>, this parameter indicates that the preshared key information will be stored in non-volatile memory and will persist across restarts of the computer or the iSCSI initiator service.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

