---
UID: NF:iscsidsc.GetIScsiSessionListA
title: GetIScsiSessionListA function
author: windows-driver-content
description: GetIscsiSessionList function retrieves the list of active iSCSI sessions.
old-location: iscsidisc\getiscsisessionlist.htm
old-project: iSCSIDisc
ms.assetid: b16b9e52-67af-4745-ac67-a2096dafe94e
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetIScsiSessionListA, GetIscsiSessionList, GetIscsiSessionList function [iSCSI Discovery Library API], GetIscsiSessionListA, GetIscsiSessionListW, iscsidisc.getiscsisessionlist, iscsidsc/GetIscsiSessionList, iscsidsc/GetIscsiSessionListA, iscsidsc/GetIscsiSessionListW
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
req.unicode-ansi: GetIscsiSessionListW (Unicode) and GetIscsiSessionListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	GetIscsiSessionList
-	GetIscsiSessionListA
-	GetIscsiSessionListW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIScsiSessionListA function


## -description


The <b>GetIscsiSessionList</b> function retrieves the list of active iSCSI sessions.



## -parameters




### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size, in bytes, of the caller-allocated buffer that <i>SessionInfo</i> points to. If the operation succeeds, the location receives the size, in bytes, of the session information data that was retrieved. 

If the operation fails because the output buffer size was insufficient, the location receives the size, in bytes, of the buffer size required to contain the output data.


### -param SessionCount [out]

A pointer to a location that, on input, contains the number of <a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a> structures that the buffer that <i>SessionInfo</i> points to can contain. If the operation succeeds, the location receives the number of <b>ISCSI_SESSION_INFO</b> structures that were retrieved.


### -param SessionInfo [out]

A pointer to a buffer that contains a series of contiguous structures of type <a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a> that describe the active login sessions. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>SessionInfo</i> was insufficient to hold the output data. 

Otherwise, <b>GetIscsiSessionList</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/5da4aa28-a630-41f2-abb2-5538c11242e6">ISCSI_SESSION_INFO</a>
 

 

