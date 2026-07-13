---
UID: NF:iscsidsc.AddISNSServerA
title: AddISNSServerA function (iscsidsc.h)
description: AddIsnsServer function adds a new server to the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets. (ANSI)
helpviewer_keywords: ["AddISNSServerA", "AddIsnsServerA", "iscsidsc/AddIsnsServerA"]
old-location: iscsidisc\addisnsserver.htm
tech.root: iSCSIDisc
ms.assetid: c01f00f9-2929-4745-a60b-89ab1143a084
ms.date: 12/05/2018
ms.keywords: AddISNSServerA, AddIsnsServer, AddIsnsServer function [iSCSI Discovery Library API], AddIsnsServerA, AddIsnsServerW, iscsidisc.addisnsserver, iscsidsc/AddIsnsServer, iscsidsc/AddIsnsServerA, iscsidsc/AddIsnsServerW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddIsnsServerW (Unicode) and AddIsnsServerA (ANSI)
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
 - AddISNSServerA
 - iscsidsc/AddISNSServerA
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
 - AddIsnsServer
 - AddIsnsServerA
 - AddIsnsServerW
---

# AddISNSServerA function


## -description

The <b>AddIsnsServer</b> function adds a new server to the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.

## -parameters

### -param Address [in]

IP address or the DNS name of the server.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. If the operation fails, because of a problem with a socket connection, <b>AddIsnsServer</b> returns a Winsock error code. If the Address parameter does not point to a valid iSNS server name, the <b>AddIsnsServer</b> routine returns ERROR_INVALID_PARAMETER.

## -remarks

When the iSCSI initiator service receives a request from the <b>AddIsnsServer</b> user-mode library function to add an iSNS server, the initiator service saves relevant data about the iSNS server in non-volatile storage. The iSCSI initiator service queries the newly added server for discovered targets immediately after adding it. From that point forward, the iSCSI initiator service automatically queries the iSNS server whenever the initiator service refreshes the target list of the iSNS server. The initiator service also refreshes the target list of the iSNS server at startup or whenever the iSNS server indicates a change.

If management software does not call <b>AddIsnsServer</b> to manually add the new iSNS servers to the service list of the iSCSI initiator service, the initiator service must rely on automatic discovery mechanisms, such as <a href="/previous-versions/windows/desktop/dhcp/about-dynamic-host-configuration-protocol">DHCP</a>, to add new iSNS servers to the list.





> [!NOTE]
> The iscsidsc.h header defines AddISNSServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-refreshisnsservera">RefreshIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeisnsservera">RemoveIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportisnsserverlista">ReportIsnsServerList</a>
