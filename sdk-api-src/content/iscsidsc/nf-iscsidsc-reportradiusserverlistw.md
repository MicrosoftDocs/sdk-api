---
UID: NF:iscsidsc.ReportRadiusServerListW
title: ReportRadiusServerListW function
author: windows-sdk-content
description: ReportRadiusServerList function retrieves the list of Remote Authentication Dail-In Service (RADIUS) servers the iSCSI initiator service uses during authentication.
old-location: iscsidisc\reportradiusserverlist.htm
old-project: iSCSIDisc
ms.assetid: 83f9fdca-805a-44ed-bd6b-0a731c63cfe6
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ReportRadiusServerList, ReportRadiusServerList function [iSCSI Discovery Library API], ReportRadiusServerListA, ReportRadiusServerListW, iscsidisc.reportradiusserverlist, iscsidsc/ReportRadiusServerList, iscsidsc/ReportRadiusServerListA, iscsidsc/ReportRadiusServerListW
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
req.unicode-ansi: ReportRadiusServerListW (Unicode) and ReportRadiusServerListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - ReportRadiusServerList
 - ReportRadiusServerListA
 - ReportRadiusServerListW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# ReportRadiusServerListW function


## -description


The <b>ReportRadiusServerList</b> function  retrieves the list of Remote Authentication Dail-In Service (RADIUS) servers the iSCSI initiator service uses during authentication.


## -parameters




### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 



### -param Buffer [out, optional]

Pointer to a buffer that receives the list of Remote Authentication Dail-In Service (RADIUS) servers on output. Each server name is null terminated, except for the last server name, which is double null-terminated.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550133">AddRadiusServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564020">RemoveRadiusServer</a>
 

 

