---
UID: NF:iscsidsc.AddISNSServerW
title: AddISNSServerW function
author: windows-sdk-content
description: AddIsnsServer function adds a new server to the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.
old-location: iscsidisc\addisnsserver.htm
old-project: iSCSIDisc
ms.assetid: c01f00f9-2929-4745-a60b-89ab1143a084
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: AddISNSServerW, AddIsnsServer, AddIsnsServer function [iSCSI Discovery Library API], AddIsnsServerA, AddIsnsServerW, iscsidisc.addisnsserver, iscsidsc/AddIsnsServer, iscsidsc/AddIsnsServerA, iscsidsc/AddIsnsServerW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	AddIsnsServer
-	AddIsnsServerA
-	AddIsnsServerW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# AddISNSServerW function


## -description


The <b>AddIsnsServer</b> function adds a new server to the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.


## -parameters




### -param Address [in]

IP address or the DNS name of the server.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. If the operation fails, because of a problem with a socket connection, <b>AddIsnsServer</b> returns a Winsock error code. If the Address parameter does not point to a valid iSNS server name, the <b>AddIsnsServer</b> routine returns ERROR_INVALID_PARAMETER.





## -remarks



When the iSCSI initiator service receives a request from the <b>AddIsnsServer</b> user-mode library function to add an iSNS server, the initiator service saves relevant data about the iSNS server in non-volatile storage. The iSCSI initiator service queries the newly added server for discovered targets immediately after adding it. From that point forward, the iSCSI initiator service automatically queries the iSNS server whenever the initiator service refreshes the target list of the iSNS server. The initiator service also refreshes the target list of the iSNS server at startup or whenever the iSNS server indicates a change.

If management software does not call <b>AddIsnsServer</b> to manually add the new iSNS servers to the service list of the iSCSI initiator service, the initiator service must rely on automatic discovery mechanisms, such as <a href="https://msdn.microsoft.com/d8eb3dde-1a69-4b10-9367-769978b25e45">DHCP</a>, to add new iSNS servers to the list.




## -see-also




<a href="https://msdn.microsoft.com/c954126a-6bad-49cf-889e-81746fe175a4">RefreshIsnsServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563978">RemoveIsnsServer</a>



<a href="https://msdn.microsoft.com/4fa773ac-0d3e-4860-8603-cb36e9278e93">ReportIsnsServerList</a>
 

 

