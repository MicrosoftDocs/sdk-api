---
UID: NF:iscsidsc.RefreshISNSServerA
title: RefreshISNSServerA function (iscsidsc.h)
description: RefreshIsnsServer function instructs the iSCSI initiator service to query the indicated Internet Storage Name Service (iSNS) server to refresh the list of discovered targets for the iSCSI initiator service. (ANSI)
helpviewer_keywords: ["RefreshISNSServerA", "RefreshIsnsServerA", "iscsidsc/RefreshIsnsServerA"]
old-location: iscsidisc\refreshisnsserver.htm
tech.root: iSCSIDisc
ms.assetid: c954126a-6bad-49cf-889e-81746fe175a4
ms.date: 12/05/2018
ms.keywords: RefreshISNSServerA, RefreshIsnsServer, RefreshIsnsServer function [iSCSI Discovery Library API], RefreshIsnsServerA, RefreshIsnsServerW, iscsidisc.refreshisnsserver, iscsidsc/RefreshIsnsServer, iscsidsc/RefreshIsnsServerA, iscsidsc/RefreshIsnsServerW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RefreshIsnsServerW (Unicode) and RefreshIsnsServerA (ANSI)
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
 - RefreshISNSServerA
 - iscsidsc/RefreshISNSServerA
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
 - RefreshIsnsServer
 - RefreshIsnsServerA
 - RefreshIsnsServerW
---

# RefreshISNSServerA function


## -description

The <b>RefreshIsnsServer</b> function instructs the iSCSI initiator service to query the indicated Internet Storage Name Service (iSNS) server to refresh the list of discovered targets for the iSCSI initiator service.

## -parameters

### -param Address [in]

The DNS or IP Address of the iSNS server.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

If the refresh succeeds, the iSCSI initiator service replaces the previous list of targets discovered by the indicated iSNS server with the updated list.

If the iSNS server supports State Change Notifications (SCN), the iSCSI initiator can keep the iSNS target list up to date, without requiring calls of the <b>RefreshIsnsServer</b> function.






> [!NOTE]
> The iscsidsc.h header defines RefreshISNSServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addisnsservera">AddIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeisnsservera">RemoveIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportisnsserverlista">ReportIsnsServerList</a>
