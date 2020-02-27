---
UID: NF:iscsidsc.RemoveISNSServerA
title: RemoveISNSServerA function (iscsidsc.h)
description: RemoveIsnsServer function removes a server from the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.
old-location: iscsidisc\removeisnsserver.htm
tech.root: iSCSIDisc
ms.assetid: 702a86e3-eeac-40cd-9203-ee865e2b710a
ms.date: 12/05/2018
ms.keywords: RemoveISNSServerA, RemoveIsnsServer, RemoveIsnsServer function [iSCSI Discovery Library API], RemoveIsnsServerA, RemoveIsnsServerW, iscsidisc.removeisnsserver, iscsidsc/RemoveIsnsServer, iscsidsc/RemoveIsnsServerA, iscsidsc/RemoveIsnsServerW
f1_keywords:
- iscsidsc/RemoveIsnsServer
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
req.unicode-ansi: RemoveIsnsServerW (Unicode) and RemoveIsnsServerA (ANSI)
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
- RemoveIsnsServer
- RemoveIsnsServerA
- RemoveIsnsServerW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveISNSServerA function


## -description


The <b>RemoveIsnsServer</b> function removes a server from the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.



## -parameters




### -param Address [in]

The DNS or IP Address of the server to remove.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>RemoveIsnsServer</b> function does not affect the list of discovered targets for the iSCSI initiator service. Targets previously discovered by the iSNS server that is being removed remain on the list of discovered targets. However, the iSNS server is also removed from the persistent list of iSNS servers.






## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addisnsservera">AddIsnsServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-refreshisnsservera">RefreshIsnsServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportisnsserverlista">ReportIsnsServerList</a>
 

 

