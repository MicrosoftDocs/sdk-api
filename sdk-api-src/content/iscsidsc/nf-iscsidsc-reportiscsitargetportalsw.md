---
UID: NF:iscsidsc.ReportIScsiTargetPortalsW
title: ReportIScsiTargetPortalsW function (iscsidsc.h)
author: windows-sdk-content
description: ReportIscsiTargetPortals function retrieves target portal information discovered by the iSCSI initiator service.
old-location: iscsidisc\reportiscsitargetportals.htm
tech.root: iSCSIDisc
ms.assetid: e52d095d-4c05-490e-bdc3-639198a93335
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ReportIScsiTargetPortalsW, ReportIscsiTargetPortals, ReportIscsiTargetPortals function [iSCSI Discovery Library API], ReportIscsiTargetPortalsA, ReportIscsiTargetPortalsW, iscsidisc.reportiscsitargetportals, iscsidsc/ReportIscsiTargetPortals, iscsidsc/ReportIscsiTargetPortalsA, iscsidsc/ReportIscsiTargetPortalsW
ms.topic: function
f1_keywords: ["iscsidsc/ReportIscsiTargetPortals"]
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiTargetPortalsW (Unicode) and ReportIscsiTargetPortalsA (ANSI)
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
 - ReportIscsiTargetPortals
 - ReportIscsiTargetPortalsA
 - ReportIscsiTargetPortalsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReportIScsiTargetPortalsW function


## -description


The <b>ReportIscsiTargetPortals</b> function retrieves target portal information discovered by the iSCSI initiator service.


## -parameters




### -param InitiatorName [in, optional]

A string that represents the name of the initiator node.


### -param TargetName [in]

A string that represents the name of the target for which the portal information is retrieved.


### -param TargetPortalTag [in, optional]

A <b>USHORT</b> value that represents a tag associated with the portal.


### -param ElementCount [in, out]

A <b>ULONG</b> value that specifies the number of portals currently reported for the specified target.


### -param Portals [out]

A variable-length array of an <b>ISCSI_TARGET_PORTALW</b> structure. The number of elements contained in this array is specified by the value of <i>ElementCount</i>.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<b>ISCSI_TARGET_PORTALW</b>
 

 

