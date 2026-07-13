---
UID: NF:iscsidsc.RemoveRadiusServerW
title: RemoveRadiusServerW function (iscsidsc.h)
description: RemoveRadiusServer function removes a Remote Authentication Dial-In User Service (RADIUS) server entry from the RADIUS server list with which an iSCSI initiator is configured. (Unicode)
helpviewer_keywords: ["RemoveRadiusServer", "RemoveRadiusServer function [iSCSI Discovery Library API]", "RemoveRadiusServerW", "iscsidisc.removeradiusserver", "iscsidsc/RemoveRadiusServer", "iscsidsc/RemoveRadiusServerW"]
old-location: iscsidisc\removeradiusserver.htm
tech.root: iSCSIDisc
ms.assetid: e096a91b-84de-4b7d-a0d6-1364746ec488
ms.date: 12/05/2018
ms.keywords: RemoveRadiusServer, RemoveRadiusServer function [iSCSI Discovery Library API], RemoveRadiusServerA, RemoveRadiusServerW, iscsidisc.removeradiusserver, iscsidsc/RemoveRadiusServer, iscsidsc/RemoveRadiusServerA, iscsidsc/RemoveRadiusServerW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveRadiusServerW (Unicode) and RemoveRadiusServerA (ANSI)
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
 - RemoveRadiusServerW
 - iscsidsc/RemoveRadiusServerW
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
 - RemoveRadiusServer
 - RemoveRadiusServerA
 - RemoveRadiusServerW
---

# RemoveRadiusServerW function


## -description

The <b>RemoveRadiusServer</b> function removes a Remote Authentication Dial-In User Service (RADIUS) server entry from the RADIUS server list with which an iSCSI initiator is configured.

## -parameters

### -param Address [in]

A string that represents the IP address or RADIUS server name.

## -returns

Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addradiusservera">AddRadiusServer</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RemoveRadiusServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
