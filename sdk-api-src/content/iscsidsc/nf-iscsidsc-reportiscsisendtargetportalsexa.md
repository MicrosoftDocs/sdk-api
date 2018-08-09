---
UID: NF:iscsidsc.ReportIScsiSendTargetPortalsExA
title: ReportIScsiSendTargetPortalsExA function
author: windows-sdk-content
description: ReportIscsiSendTargetPortalsEx function retrieves a list of static target portals that the iSCSI initiator service uses to perform automatic discovery with SendTarget requests.
old-location: iscsidisc\reportiscsisendtargetportalsex.htm
old-project: iSCSIDisc
ms.assetid: bf67ff5c-77b5-42ec-81b3-86b98e216d81
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ReportIScsiSendTargetPortalsExA, ReportIscsiSendTargetPortalsEx, ReportIscsiSendTargetPortalsEx function [iSCSI Discovery Library API], ReportIscsiSendTargetPortalsExA, ReportIscsiSendTargetPortalsExW, iscsidisc.reportiscsisendtargetportalsex, iscsidsc/ReportIscsiSendTargetPortalsEx, iscsidsc/ReportIscsiSendTargetPortalsExA, iscsidsc/ReportIscsiSendTargetPortalsExW
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
req.unicode-ansi: ReportIscsiSendTargetPortalsExW (Unicode) and ReportIscsiSendTargetPortalsExA (ANSI)
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
 - ReportIscsiSendTargetPortalsEx
 - ReportIscsiSendTargetPortalsExA
 - ReportIscsiSendTargetPortalsExW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# ReportIScsiSendTargetPortalsExA function


## -description


The <b>ReportIscsiSendTargetPortalsEx</b> function  retrieves a list of static target portals that the iSCSI initiator service uses to perform automatic discovery with <b>SendTarget</b> requests.


## -parameters




### -param PortalCount [out]

A pointer to a location that, on input, contains the number of entries in the <i>PortalInfo</i> array. On output, this parameter specifies the number of elements that contain return data. 


### -param PortalInfoSize [in, out]

A pointer to a location that, on input, contains the byte-size of the buffer specified by <i>PortalInfo</i>. On output, this parameter specifies the number of bytes retrieved. 


### -param PortalInfo [in, out]

Pointer to an array of elements contained in a <a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO_EX</a> structure that describe the portals that the iSCSI initiator service utilizes to perform discovery with <b>SendTargets</b> requests. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>PortalInfo</i> is insufficient to contain the output data. Otherwise, <b>ReportIscsiSendTargetPortalsEx</b> returns the appropriate Win32 or iSCSI error code on failure.





## -see-also




<a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO_EX</a>
 

 

