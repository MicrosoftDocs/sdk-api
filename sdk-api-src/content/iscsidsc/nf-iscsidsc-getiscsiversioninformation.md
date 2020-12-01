---
UID: NF:iscsidsc.GetIScsiVersionInformation
title: GetIScsiVersionInformation function (iscsidsc.h)
description: GetIscsiVersionInformation function retrieves information about the initiator version.
helpviewer_keywords: ["GetIScsiVersionInformation","GetIscsiVersionInformation","GetIscsiVersionInformation function [iSCSI Discovery Library API]","iscsidisc.getiscsiversioninformation","iscsidsc/GetIscsiVersionInformation"]
old-location: iscsidisc\getiscsiversioninformation.htm
tech.root: iSCSIDisc
ms.assetid: b1b17aa4-1aa8-440e-a9d8-f11c03e48afc
ms.date: 12/05/2018
ms.keywords: GetIScsiVersionInformation, GetIscsiVersionInformation, GetIscsiVersionInformation function [iSCSI Discovery Library API], iscsidisc.getiscsiversioninformation, iscsidsc/GetIscsiVersionInformation
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
 - GetIScsiVersionInformation
 - iscsidsc/GetIScsiVersionInformation
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
 - GetIscsiVersionInformation
---

# GetIScsiVersionInformation function


## -description

The <b>GetIscsiVersionInformation</b> function retrieves information about the initiator version.

## -parameters

### -param VersionInfo

Pointer to an <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_version_info">ISCSI_VERSION_INFO</a> structure that contains  initiator version information.

## -returns

Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_version_info">ISCSI_VERSION_INFO</a>