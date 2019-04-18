---
UID: NF:iscsidsc.ReportIScsiSendTargetPortalsW
title: ReportIScsiSendTargetPortalsW function (iscsidsc.h)
author: windows-sdk-content
description: ReportIscsiSendTargetPortals function retrieves a list of target portals that the iSCSI initiator service uses to perform automatic discovery with SendTarget requests.
old-location: iscsidisc\reportiscsisendtargetportals.htm
tech.root: iSCSIDisc
ms.assetid: f082acc3-98d6-4758-aded-cb83e150e6d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReportIScsiSendTargetPortalsW, ReportIscsiSendTargetPortals, ReportIscsiSendTargetPortals function [iSCSI Discovery Library API], ReportIscsiSendTargetPortalsA, ReportIscsiSendTargetPortalsW, iscsidisc.reportiscsisendtargetportals, iscsidsc/ReportIscsiSendTargetPortals, iscsidsc/ReportIscsiSendTargetPortalsA, iscsidsc/ReportIscsiSendTargetPortalsW
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiSendTargetPortalsW (Unicode) and ReportIscsiSendTargetPortalsA (ANSI)
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
 - ReportIscsiSendTargetPortals
 - ReportIscsiSendTargetPortalsA
 - ReportIscsiSendTargetPortalsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReportIScsiSendTargetPortalsW function


## -description


The <b>ReportIscsiSendTargetPortals</b> function retrieves a list of target portals that the iSCSI initiator service uses to perform automatic discovery with <b>SendTarget</b> requests.



## -parameters




### -param PortalCount [out]

A pointer to a location that, on input, contains the number of entries in the <i>PortalInfo</i> array. On output, this parameter specifies the number of elements that contain return data. 


### -param PortalInfo [in, out]

Pointer to an array of elements contained in <a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO</a> structures that describe the portals that the iSCSI initiator service utilizes to perform discovery with <b>SendTargets</b> requests. 


## -returns



 Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size of Buffer is insufficient to contain the output data.




## -see-also




<a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO</a>
 

 

