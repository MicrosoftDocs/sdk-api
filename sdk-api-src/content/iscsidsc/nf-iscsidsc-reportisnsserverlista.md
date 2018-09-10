---
UID: NF:iscsidsc.ReportISNSServerListA
title: ReportISNSServerListA function
author: windows-sdk-content
description: ReportIsnsServerList function retrieves the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service queries for discovered targets.
old-location: iscsidisc\reportisnsserverlist.htm
tech.root: iSCSIDisc
ms.assetid: 4fa773ac-0d3e-4860-8603-cb36e9278e93
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ReportISNSServerListA, ReportIsnsServerList, ReportIsnsServerList function [iSCSI Discovery Library API], ReportIsnsServerListA, ReportIsnsServerListW, iscsidisc.reportisnsserverlist, iscsidsc/ReportIsnsServerList, iscsidsc/ReportIsnsServerListA, iscsidsc/ReportIsnsServerListW
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
req.unicode-ansi: ReportIsnsServerListW (Unicode) and ReportIsnsServerListA (ANSI)
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
 - ReportIsnsServerList
 - ReportIsnsServerListA
 - ReportIsnsServerListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReportISNSServerListA function


## -description


The <b>ReportIsnsServerList</b> function retrieves the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service queries for discovered targets.



## -parameters




### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 
If the operation succeeds, this location receives the size, represented by a number of  elements, that corresponds to the number of retrieved iSNS servrs.


### -param Buffer [out]

The buffer that holds the list of iSNS servers on output. Each server name is <b>null</b> terminated, except for the last server name, which is double <b>null</b> terminated. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is too small to hold the output data. 

Otherwise, <b>ReportIsnsServerList</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/c01f00f9-2929-4745-a60b-89ab1143a084">AddIsnsServer</a>



<a href="https://msdn.microsoft.com/c954126a-6bad-49cf-889e-81746fe175a4">RefreshIsnsServer</a>



<a href="https://msdn.microsoft.com/702a86e3-eeac-40cd-9203-ee865e2b710a">RemoveIsnsServer</a>
 

 

