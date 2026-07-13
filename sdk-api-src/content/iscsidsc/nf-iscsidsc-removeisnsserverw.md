---
UID: NF:iscsidsc.RemoveISNSServerW
title: RemoveISNSServerW function (iscsidsc.h)
description: RemoveIsnsServer function removes a server from the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets. (Unicode)
helpviewer_keywords: ["RemoveISNSServerW", "RemoveIsnsServer", "RemoveIsnsServer function [iSCSI Discovery Library API]", "RemoveIsnsServerW", "iscsidisc.removeisnsserver", "iscsidsc/RemoveIsnsServer", "iscsidsc/RemoveIsnsServerW"]
old-location: iscsidisc\removeisnsserver.htm
tech.root: iSCSIDisc
ms.assetid: 702a86e3-eeac-40cd-9203-ee865e2b710a
ms.date: 12/05/2018
ms.keywords: RemoveISNSServerW, RemoveIsnsServer, RemoveIsnsServer function [iSCSI Discovery Library API], RemoveIsnsServerA, RemoveIsnsServerW, iscsidisc.removeisnsserver, iscsidsc/RemoveIsnsServer, iscsidsc/RemoveIsnsServerA, iscsidsc/RemoveIsnsServerW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveIsnsServerW (Unicode) and RemoveIsnsServerA (ANSI)
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
 - RemoveISNSServerW
 - iscsidsc/RemoveISNSServerW
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
 - RemoveIsnsServer
 - RemoveIsnsServerA
 - RemoveIsnsServerW
---

# RemoveISNSServerW function


## -description

The <b>RemoveIsnsServer</b> function removes a server from the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.

## -parameters

### -param Address [in]

The DNS or IP Address of the server to remove.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

The <b>RemoveIsnsServer</b> function does not affect the list of discovered targets for the iSCSI initiator service. Targets previously discovered by the iSNS server that is being removed remain on the list of discovered targets. However, the iSNS server is also removed from the persistent list of iSNS servers.







> [!NOTE]
> The iscsidsc.h header defines RemoveISNSServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addisnsservera">AddIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-refreshisnsservera">RefreshIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportisnsserverlista">ReportIsnsServerList</a>
