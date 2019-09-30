---
UID: NF:iscsidsc.ReportRadiusServerListW
title: ReportRadiusServerListW function (iscsidsc.h)
author: windows-sdk-content
description: ReportRadiusServerList function retrieves the list of Remote Authentication Dail-In Service (RADIUS) servers the iSCSI initiator service uses during authentication.
old-location: iscsidisc\reportradiusserverlist.htm
tech.root: iSCSIDisc
ms.assetid: 83f9fdca-805a-44ed-bd6b-0a731c63cfe6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReportRadiusServerList, ReportRadiusServerList function [iSCSI Discovery Library API], ReportRadiusServerListA, ReportRadiusServerListW, iscsidisc.reportradiusserverlist, iscsidsc/ReportRadiusServerList, iscsidsc/ReportRadiusServerListA, iscsidsc/ReportRadiusServerListW
ms.topic: function
f1_keywords: 
 - "iscsidsc/ReportRadiusServerList"
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
 - ReportRadiusServerList
 - ReportRadiusServerListA
 - ReportRadiusServerListW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addradiusservera">AddRadiusServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeradiusservera">RemoveRadiusServer</a>
 

 

