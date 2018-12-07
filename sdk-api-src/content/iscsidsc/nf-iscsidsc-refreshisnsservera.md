---
UID: NF:iscsidsc.RefreshISNSServerA
title: RefreshISNSServerA function
author: windows-sdk-content
description: RefreshIsnsServer function instructs the iSCSI initiator service to query the indicated Internet Storage Name Service (iSNS) server to refresh the list of discovered targets for the iSCSI initiator service.
old-location: iscsidisc\refreshisnsserver.htm
tech.root: iSCSIDisc
ms.assetid: c954126a-6bad-49cf-889e-81746fe175a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RefreshISNSServerA, RefreshIsnsServer, RefreshIsnsServer function [iSCSI Discovery Library API], RefreshIsnsServerA, RefreshIsnsServerW, iscsidisc.refreshisnsserver, iscsidsc/RefreshIsnsServer, iscsidsc/RefreshIsnsServerA, iscsidsc/RefreshIsnsServerW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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





## -see-also




<a href="https://msdn.microsoft.com/c01f00f9-2929-4745-a60b-89ab1143a084">AddIsnsServer</a>



<a href="https://msdn.microsoft.com/702a86e3-eeac-40cd-9203-ee865e2b710a">RemoveIsnsServer</a>



<a href="https://msdn.microsoft.com/4fa773ac-0d3e-4860-8603-cb36e9278e93">ReportIsnsServerList</a>
 

 

