---
UID: NF:iscsidsc.GetIScsiVersionInformation
title: GetIScsiVersionInformation function
author: windows-sdk-content
description: GetIscsiVersionInformation function retrieves information about the initiator version.
old-location: iscsidisc\getiscsiversioninformation.htm
old-project: iSCSIDisc
ms.assetid: b1b17aa4-1aa8-440e-a9d8-f11c03e48afc
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: GetIScsiVersionInformation, GetIscsiVersionInformation, GetIscsiVersionInformation function [iSCSI Discovery Library API], iscsidisc.getiscsiversioninformation, iscsidsc/GetIscsiVersionInformation
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
req.unicode-ansi: 
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
 - GetIscsiVersionInformation
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIScsiVersionInformation function


## -description


The <b>GetIscsiVersionInformation</b> function retrieves information about the initiator version.


## -parameters




### -param VersionInfo

Pointer to an <a href="https://msdn.microsoft.com/04b9e0c0-2c1e-4553-8eef-697819075bc4">ISCSI_VERSION_INFO</a> structure that contains  initiator version information.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<a href="https://msdn.microsoft.com/04b9e0c0-2c1e-4553-8eef-697819075bc4">ISCSI_VERSION_INFO</a>
 

 

