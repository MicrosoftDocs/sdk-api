---
UID: NF:iscsidsc.ClearPersistentIScsiDevices
title: ClearPersistentIScsiDevices function (iscsidsc.h)
description: ClearPersistentIscsiDevices function removes all volumes and devices from the list of persistently bound iSCSI volumes.
helpviewer_keywords: ["ClearPersistentIScsiDevices","ClearPersistentiScsiDevices","ClearPersistentiScsiDevices function [iSCSI Discovery Library API]","iscsidisc.clearpersistentiscsidevices","iscsidsc/ClearPersistentiScsiDevices"]
old-location: iscsidisc\clearpersistentiscsidevices.htm
tech.root: iSCSIDisc
ms.assetid: 9e21dde6-face-40ae-803b-2aa7861e6f4f
ms.date: 12/05/2018
ms.keywords: ClearPersistentIScsiDevices, ClearPersistentiScsiDevices, ClearPersistentiScsiDevices function [iSCSI Discovery Library API], iscsidisc.clearpersistentiscsidevices, iscsidsc/ClearPersistentiScsiDevices
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClearPersistentIScsiDevices
 - iscsidsc/ClearPersistentIScsiDevices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - ClearPersistentiScsiDevices
---

# ClearPersistentIScsiDevices function


## -description

The <b>ClearPersistentIscsiDevices</b> function removes all volumes and devices from the list of persistently bound iSCSI volumes.



## -returns

returns ERROR_SUCCESS if the operation succeeds and the appropriate Win32 or iSCSI error code if the operation fails.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removepersistentiscsidevicea">RemovePersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>
