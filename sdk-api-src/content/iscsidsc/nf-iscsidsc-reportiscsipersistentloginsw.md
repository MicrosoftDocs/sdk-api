---
UID: NF:iscsidsc.ReportIScsiPersistentLoginsW
title: ReportIScsiPersistentLoginsW function
author: windows-sdk-content
description: ReportIscsiPersistentLogins function retrieves the list of persistent login targets.
old-location: iscsidisc\reportiscsipersistentlogins.htm
tech.root: iSCSIDisc
ms.assetid: 0ab1a864-b44e-4307-9f7c-93cc0d40ff3a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ReportIScsiPersistentLoginsW, ReportIscsiPersistentLogins, ReportIscsiPersistentLogins function [iSCSI Discovery Library API], ReportIscsiPersistentLoginsA, ReportIscsiPersistentLoginsW, iscsidisc.reportiscsipersistentlogins, iscsidsc/ReportIscsiPersistentLogins, iscsidsc/ReportIscsiPersistentLoginsA, iscsidsc/ReportIscsiPersistentLoginsW
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
req.unicode-ansi: ReportIscsiPersistentLoginsW (Unicode) and ReportIscsiPersistentLoginsA (ANSI)
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
 - ReportIscsiPersistentLogins
 - ReportIscsiPersistentLoginsA
 - ReportIscsiPersistentLoginsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ReportIScsiPersistentLoginsW
: 
---

# ReportIScsiPersistentLoginsW function


## -description


The <b>ReportIscsiPersistentLogins</b> function retrieves the list of persistent login targets.



## -parameters




### -param Count [out]

A pointer to the location that receives a count of the elements specified by  <i>PersistentLoginInfo</i>.


### -param PersistentLoginInfo [in, out]

An array of <a href="https://msdn.microsoft.com/adfd57fb-18dc-440f-988e-f2c01698d987">PERSISTENT_ISCSI_LOGIN_INFO</a> structures that, on output, describe the persistent login targets.


### -param BufferSizeInBytes [in, out]

A pointer to a location that, on input, contains the byte-size of the buffer space that <i>PersistentLoginInfo</i>  specifies. If the buffer size is insufficient, this parameter specifies what is  required to contain the output data. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer specified by <i>PersistentLoginInfo</i> is insufficient to contain the output data. 

Otherwise, <b>ReportIscsiPersistentLogins</b> returns the appropriate Win32 or iSCSI error code on failure.




## -remarks



The <a href="https://msdn.microsoft.com/adfd57fb-18dc-440f-988e-f2c01698d987">PERSISTENT_ISCSI_LOGIN_INFO</a> structure provides an initiator with the information required to log in to a target each time the initiator device is started.




## -see-also




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/adfd57fb-18dc-440f-988e-f2c01698d987">PERSISTENT_ISCSI_LOGIN_INFO</a>



<a href="https://msdn.microsoft.com/2522f906-2a91-4d5b-8d6b-86e22c707046">RemoveIscsiPersistentTarget</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

