---
UID: NF:iscsidsc.AddRadiusServerA
title: AddRadiusServerA function (iscsidsc.h)
description: AddRadiusServer. (ANSI)
helpviewer_keywords: ["AddRadiusServerA", "iscsidsc/AddRadiusServerA"]
old-location: iscsidisc\addradiusserver.htm
tech.root: iSCSIDisc
ms.assetid: ed89b329-f1ea-4606-b305-a245d29b119c
ms.date: 12/05/2018
ms.keywords: AddRadiusServer, AddRadiusServer function [iSCSI Discovery Library API], AddRadiusServerA, AddRadiusServerW, iscsidisc.addradiusserver, iscsidsc/AddRadiusServer, iscsidsc/AddRadiusServerA, iscsidsc/AddRadiusServerW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddRadiusServerW (Unicode) and AddRadiusServerA (ANSI)
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
 - AddRadiusServerA
 - iscsidsc/AddRadiusServerA
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
 - AddRadiusServer
 - AddRadiusServerA
 - AddRadiusServerW
---

# AddRadiusServerA function


## -description

The <b>AddRadiusServer</b> function adds a new Remote Authentication Dial-In User Service (RADIUS)  server to the list referenced by the iSCSI initiator service during authentication.

## -parameters

### -param Address [in]

A string that represents the IP address or DNS name associated with the RADIUS server.

## -returns

Returns ERROR_SUCCESS if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code. Other possible error values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>Address</i> is invalid.

</td>
</tr>
</table>

## -remarks

When the iSCSI initiator service receives a request from the <b>AddRadiusServer</b> user-mode library function to add a RADIUS server, the initiator service saves data associated with the server in non-volatile storage. This allows the iSCSI initiator service to utilize the RADIUS server to authenticate targets or obtain authentication information.





> [!NOTE]
> The iscsidsc.h header defines AddRadiusServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeradiusservera">RemoveRadiusServer</a>
